---
title: useEffect hook tricks
date: 2022-04-07 12:01:05
banner_img: https://dogefs.s3.ladydaily.com/~/source/unsplash/photo-1648737154547-b0dfd281c51e?ixlib=rb-1.2.1&ixid=MnwxMjA3fDF8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=870&q=80
index_img: https://dogefs.s3.ladydaily.com/~/source/unsplash/photo-1648737154547-b0dfd281c51e?ixlib=rb-1.2.1&ixid=MnwxMjA3fDF8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=870&q=80
tags: [React, Javascript]
categories: React Tricks
---

Today, I would like to show one trick of using useEffect hook in react. When we do want to run the side effect function in different conditions, we usually add dependencies to the second parameter of the useEffect hook. However, it does not prevent it from running when the component first time loaded. If we do not want to run the callback function, we will need to customize the useEffect hook.

```
function useDidUpdateEffect(fn, inputs) {
    const didMountRef = useRef(false);
    useEffect(() => {
        if (didMountRef.current) fn();
        else didMountRef.current = true;
    }, inputs);
}
```

once we have this new useDidUpdateEffect hook, we can use it like this:

```
useDidUpdateEffect(() => {
    // your function goes here
    
    }, [//dependency goes here]);