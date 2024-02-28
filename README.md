import React, { useState } from 'react'

export default function App() {
  const[FormData,Setform]=useState({
    name:'',
    email:'',
    phone:'',
    address:'',
  })

  const handlechange=(event)=>{
console.log(event.target.value)
    const{name,value}=event.target;
Setform((InputData)=>({...InputData,[name]:value}))
  }

  const handlesubmit=(event)=>{
    event.preventDefault();
    console.log(FormData)
  }
  return (
    <div>
    
    <form action="" onClick={handlesubmit}>
    <input type="text" name="name" id="" value={FormData.name} onChange={handlechange}  />
    <input type="email" name="email" id="" value={FormData.email} onChange={handlechange}  />
    <input type="number" name="phone" id="" value={FormData.phone} onChange={handlechange}  />
    <input type="text" name="address" id="" value={FormData.address} onChange={handlechange}  />
   <button type='submit'>Submit Data</button>
    </form>
    </div>
  )
}
