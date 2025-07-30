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
const fetch_data= async () => {
    const response= await fetch("https://randomuser.me/api")
    const data=await response.json()
    console.log(data);
    
    setUser(data.results[0])
    
  }

if u have set your useState initial as null then before fetching api first check if data is available.
{user?(<div>
    <h2>User name :{user.name.first} {user.name.last}</h2>
    <h2>User email :{user.email}</h2>
    <h2>Gender :{user.gender}</h2>
    <h3>location : {user.location.city},{user.location.state}</h3>
    </div>):
    (  <p>Still loading..........</p>
    )}

//React Router:
