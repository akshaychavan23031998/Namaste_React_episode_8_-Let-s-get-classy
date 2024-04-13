# **Episode 08:-**

### **useEffectHooks:-**

the default nature of useeffect hooks is to be called after render every time.

it takes2 parameters1st is call back function which is must and2nd is dependancy array which is not mandatary we can and we can not use it according to our use case.

#### **Case1:-** No dependancy array, this will be called after each render the component is rendered.

ex:-useEffect ({} => {

  console.log("useEffect Called");

})

#### **Case2:- empty dependancy array, this will be called only once in the start of page refresh means in initial render.**

ex:-useEffect ({} => {

  console.log("useEffect Called");

}, []);

#### **Case3:- dependancy array with value, this will be called when ever the value changes, for ex login/logout btn.**

ex:- useEffect ({} => {

  console.log("useEffect Called");

},[btnName]);

### **In depth of useEffect:-**

    useEffect(() => {

    console.log("useEffcect");

    consttimer =setInterval(() => {

    console.log("Namaste React");

    },1000);

    return () => {

    clearInterval(timer);

    // to clear our above internval we can use this return statement

    console.log("use effect called after component change");

    };

    }, [])

    console.log("Render")

//Output:-

**Render, useEffcect, return(this return block of code will be called after component change).**
