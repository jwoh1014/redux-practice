# redux-practice

## Redux-practice Script입니다.

### Provider
import {Provider} from 'react-redux'
    <Provider store = {store}>
     <App />
    </Provider>
    
### Reducer
(example)
    function reducer(state = 초기값, 액션){ <br/>
    if (액션.type === '항목추가'){<br/>
      let copy = [ ...state ]<br/>
      copy.push();<br/>
      return copy<br/>
    }
     else if (액션.type === '수량증가'){<br/>
       let copy = [...state]<br/>
       copy[0].quan++;<br/>
       return copy<br/>
     } else if(액션.type === '수량감소'){<br/>
      let copy = [...state]<br/>
      copy[0].quan--;<br/>
      return copy<br/>
     } else {<br/>
         return state<br/>
     }<br/>
    }<br/>
<br/>
    let store = createStore(combineReducers({reducer, reducer2}));
    
### useSelector, useDispatch

import { connect, useDispatch } from 'react-redux';
import {useSelector} from 'react-redux'

function Cart (props){<br/>
  let state = useSelector((state) => state )<br/>
  console.log(state.reducer)<br/>
  let dispatch = useDispatch();<br/>
