# vue3-component-advanced-exercise

## Exercise N°6

1. Copy paste the `UserItem.vue` & `UserList.vue` from the previous exercise into `src/components/user`.

2. Create a component `BaseDialog.vue` into the `src/components/UI` folder. 
This component will use a `named slot` for header and a `default slot` for content, and another `named slot` for footer (button).
Use the `teleport` component to attach the dialog to the body.
Hint: You can use the html `dialog` tag [Documentation](https://developer.mozilla.org/fr/docs/Web/HTML/Element/dialog)
Emit a `close` event, when user clicks outside the dialog.

3. Move the `users` array from `UserList.vue` to `App.vue`.

4. Provide `users` array into the dependency injection from `App.vue`. 
Retrieve the `users` from the dependency injection into `UserList.vue`.

5. Use `BaseDialog` component into `UserList.vue`.
Put a title in the header slot.
Put a message in the default content `slot`.
Put a `confirm button` on footer slot.
On the confirm button, call a method to remove the user form the injected `users` array (Hint : use `array.splice` instead of `array.filter`)
Use `v-if` to check if the dialog should be shown, when event `delete-user` is emitted.
Listen `close` event to hide dialog.

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).
