# Single Page Applications with Vue
01. What is the entrypoint of an application?

  > OnMounted

02. What is the difference between a vue `component` and `page`?

  > Page i s what is shown on the html browser. Component is data used to populate the page.

03. What is ***Component-Based Architecture***?

  > reuseable codes

04. What are the three tags that make up a Vue component?

  > Template, Script, Style

05. What are ***lifecycle hooks***? What are lifecycle hooks used for?

  > lifecycle hook - onMounted= run code as soon as page mounts or renders.

06. Which component in Vue does the vue-router use to mount pages onto?

  > router.js.  router-link

07. What is the difference between the `AppState` and the state object within a component?

  > AppState holds data

08. What is the responsibility of `Services` in our Vue projects?

  > To manipulate data.

09. What are ***props*** and how are they used? Provide an example

  > Props pass variables and other information around between different components.

10. What is the Vue method used to create watchable objects such as `state` or `AppState`?

  >watchEffect(() => {
      editable.value = { ...AppState.account }
    })
