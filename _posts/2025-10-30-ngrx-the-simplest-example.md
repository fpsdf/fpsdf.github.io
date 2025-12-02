---
title: "NgRx: the simplest example"
layout: post
---

part 1: the NgRx way

here's the absolute simplest NgRx example — a todo list:

```
// actions
export const addTodo = createAction('[Todo] Add', props<{text: string}>());
export const toggleTodo = createAction('[Todo] Toggle', props<{id: number}>());

// reducer
export const todoReducer = createReducer(
  initialState,
  on(addTodo, (state, {text}) => [...state, {id: Date.now(), text, done: false}]),
  on(toggleTodo, (state, {id}) => state.map(t => t.id === id ? {...t, done: !t.done} : t))
);

// selectors
export const selectTodos = (state: AppState) => state.todos;

// component
todos$ = this.store.select(selectTodos);

addTodo(text: string) {
  this.store.dispatch(addTodo({text}));
}
```

files needed:

- todo.actions.ts
- todo.reducer.ts
- todo.selectors.ts
- todo.state.ts
- Register in app.config.ts
- Use in component

---

part 2: the normal way

Here's the same thing with a service:

```html
@Injectable({providedIn: 'root'})
export class TodoService {
  private todos = signal<Todo[]>([]);

  readonly todos$ = computed(() => this.todos());

  addTodo(text: string) {
    this.todos.update(todos => [...todos, {
      id: Date.now(),
      text,
      done: false
    }]);
  }

  toggleTodo(id: number) {
    this.todos.update(todos =>
      todos.map(t => t.id === id ? {...t, done: !t.done} : t)
    );
  }
}

// component
todos = this.todoService.todos$;

addTodo(text: string) {
  this.todoService.addTodo(text);
}
```

files needed:

- todo.service.ts
- that's it.

---

part 3: Still want NgRx?

NgRx gives:

&nbsp;&nbsp;&nbsp;✓ DevTools time-travel debugging<br />
&nbsp;&nbsp;&nbsp;✓ Enforced unidirectional data flow<br />
&nbsp;&nbsp;&nbsp;✓ Action log / audit trail<br />
&nbsp;&nbsp;&nbsp;✓ Effect handling for side effects

and it costs:

&nbsp;&nbsp;&nbsp;⨉ 5x more boilerplate<br />
&nbsp;&nbsp;&nbsp;⨉ Steeper learning curve for the team<br />
&nbsp;&nbsp;&nbsp;⨉ Harder to refactor<br />
&nbsp;&nbsp;&nbsp;⨉ More files to jump between

---
