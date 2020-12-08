# vue3-component-advanced-exercise

## Exercise N°6

1. Copy paste the `UserItem.vue` & `UserList.vue` from the previous exercise into `src/components`.

2. Create a component `BaseDialog.vue` into the `src/UI` folder. 
This component will use a `named slot` for header and a `default slot` for content, and another `named slot` for footer (buttons).
Use the `teleport` component to attach the dialog to the body.
Hint: You can use the html `dialog` tag [Documentation](https://developer.mozilla.org/fr/docs/Web/HTML/Element/dialog)

3. Move the `users` array from `UserList.vue` to `App.vue`.

4. Provide `users` array into the dependency injection from `App.vue`. 
Retrieve the `users` from the dependency injection into `UserList.vue`.

5. Use `BaseDialog` component into `UserItem.vue`, if the user clicked on `Remove User` button. The dialog will display a `cancel` & a `confirm` button. On the cancel button dialog will be closed. On the confirm button, the event `delete-user` will be emitted. 

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
