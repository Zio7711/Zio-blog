---
title: mapbox with react
date: 2022-04-03 19:59:24
banner_img: https://images.unsplash.com/photo-1517694712202-14dd9538aa97?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=870&q=80
index_img: https://images.unsplash.com/photo-1517694712202-14dd9538aa97?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=870&q=80
tags: [Mapbox, Javascript]
categories: JavaScript Fundamentals
---

Today, I was asked by my friends to take look at the implementation of a react app with mapping function that can track somebody's moves. I want to share some of my thoughts of this project.

At the beginning, I thought it was pretty easy since I had some experience with google maps api. This task was only to add tracking feature. The main point was to capture user's current location every second. Just create an Interval by

```

[currentLocation, setCurrentLocation] = useState(null)
[movingPoints, setMovingPoints] = useState(null)

useEffect( () => {

    setInterval(() => {
        //get current location
        const {long, lat} = getCurrentLocation()

        //set current location
        setCurrentLocation({long,lat})
        
        //push the current location to moving points array
        setMovingPoints([...movingPoints, {long,lat}])
    }, 1000)

}, [])

```
However, I wouldn't work for me. I kept getting the same location even though the I have moved around.

The problem was the value stored in setInterval was out dated which was caused by stale state.

The following code would solve the issue.

```
useEffect( () => {

    setInterval(() => {
        //get current location
        const {long, lat} = getCurrentLocation()

        //set current location
        setCurrentLocation({long,lat})
        
        //push the current location to moving points array
        setMovingPoints(prev => [...prev, {long, lat}])
    }, 1000)

}, [])

```

