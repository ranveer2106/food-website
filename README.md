# food-website

import React, { useState } from 'react'
import image1 from "./images/img1.jpg"
import image2 from "./images/img2.jpg"
import image3 from "./images/img3.jpg"
import './components.css'

export default function Navbar() {
    const [first, setfirst] = useState("leftone");
    const [second, setsecond] = useState("middleone")

    const gg =() =>{
        setfirst("middleone");
        setsecond("leftone");
    }

  return (
    <>
        <div className='flex justify-between py-6 px-40 border-b-4'>
            <div>
                <a href="/">Logo</a> 
            </div>
            <div>
                <ul className='flex'>
                    <li className='mx-4'><a href="/">home </a> </li>
                    <li className='mx-4'><a href="/">Order </a> </li>
                    <li className='mx-4'><a href="/">contact Us </a> </li>
                </ul>
            </div>
            <div>
                <ul className='flex'>
                    <li className='mx-4'><a href="/">Login </a></li>
                    <li className='mx-4'><a href="/">Cart </a></li> 
                </ul>
            </div>
            
        </div>
        <div className='flex one overflow-hidden max-h-48	'>
            <img src={image1} alt="img1" className={`w-screen ${first}`}/>
            <img src={image2} alt="img1" className={`w-screen ${second}`}/>
            <img src={image3} alt="img1" className='w-screen rightone'/>
        </div>
        <button onClick={gg} className='border'>do it</button>
    </>
  )
}








.leftone{
    position: absolute;
    left: -100%;
}
.middleone{
    position:  relative;
    left: 0%;
}
.rightone{
    position: relative;
    left: 100%;
}
