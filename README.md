# redux-practice

## Redux-practice Script입니다.

### Provider
import {Provider} from 'react-redux'
    <Provider store = {store}>
     <App />
    </Provider>
    
### Reducer
(example)
    function reducer(state = 초기값, 액션){
    if (액션.type === '항목추가'){
      let copy = [ ...state ]
      copy.push();
      return copy
    }
     else if (액션.type === '수량증가'){
       let copy = [...state]
       copy[0].quan++;
       return copy
     } else if(액션.type === '수량감소'){
      let copy = [...state]
      copy[0].quan--;
      return copy
     } else {
         return state
     }
    }

    let store = createStore(combineReducers({reducer, reducer2}));
    
### useSelector, useDispatch

import { connect, useDispatch } from 'react-redux';
import {useSelector} from 'react-redux'

function Cart (props){
  let state = useSelector((state) => state )
  console.log(state.reducer)
  let dispatch = useDispatch();
