"# usePersistedState-react-hook"
Use the useState() hook to initialize the value to defaultValue.
Use the useRef() hook to create a ref that will hold the name of the value in Window.localStorage.
Use 3 instances of the useEffect() hook for initialization, value change and name change respectively.
When the component is first mounted, use Storage.getItem() to update value if there's a stored value or Storage.setItem() to persist the current value.
When value is updated, use Storage.setItem() to store the new value.
When name is updated, use Storage.setItem() to create the new key, update the nameRef and use Storage.removeItem() to remove the previous key from Window.localStorage.
Note: The hook is meant for use with primitive values (i.e. not objects) and doesn't account for changes to Window.localStorage due to other code. Both of these issues can be easily handled (e.g. JSON serialization and handling the 'storage' event).
