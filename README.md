React Hooks

1)Usestate hook
const [time,setTime]=useState(new Date())


i.setCount(prev=>prev+1)

ii.onClick={()=>{random_color();countChange();}} //Way to add two functions at a time to listener.

iii.onKeyDown={(e)=>{
    if(e.key==='Enter')
    {InputCount();}
    }}/>

2)UseEffect hook

i.| Dependency Array    | Behavior                           |
  | ------------------- | ---------------------------------- |
  | `[]`                | Run only once (after first render) |
  | `[someVar]`         | Run when `someVar` changes         |
  | *(no array at all)* | Run on **every render**            |

ii.
| What you want to do                  | `useEffect`pattern                  |
| ------------------------------------ |------------------------------------ |
| Do something once on mount           | `useEffect(() => { ... }, []);`     |
| Do something when a variable changes | `useEffect(() => { ... }, [value]);`|
| Cleanup something (like a timer)     | `return () => { cleanup }` inside it|

//Random -Fetching API
