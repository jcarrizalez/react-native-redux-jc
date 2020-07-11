## Getting started

```
npm install react-native-redux-jc;
```
or
```
yarn add react-native-redux-jc
```

### Usage
```
import redux from "react-native-redux-jc";
```
Add your initial storage in the index of your project

### Initial state settings, example
```
redux.store({
  environment:env,
  storage_cache:[],
  requests_executed:[],
  prices:{data:[]},
  path:'',
  sessions:{},
  authorize:{},
  pag_count:10, 
  pag_position:'top', 
  list_type:'table'
});
```

### Insert data

```
redux.push('sessions', {username:jc, data:'example'});
```
### Insert data and store in localstorage 

```
redux.push('sessions', {username:jc, data:'example'}, true);
```

### Query data

```
redux.get('sessions');
```
### Query data, if it is null query the localstorage

```
redux.get('sessions', true);
```

### See all data

```
redux.all();
```

### add event listener

```
const unsubscribe = redux.subscribe( () => {
  if(redux.is('sessions')){
    console.log('is event);
  }
});
```
### remove event listener

```
unsubscribe();
```


