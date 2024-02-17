## ⚛️ My personal Repository for reactJS 

![Logo](https://www.vhv.rs/dpng/d/612-6126558_react-logo-png-react-js-logo-svg-transparent.png)


🥏**Replit :**
[Replit](https://replit.com/@KinshukTheAlpha) 

🥏**LinkedIn :**
[LinkedIn](https://www.linkedin.com/in/kinshuk-j-1966981b4/)


## Best Hooks to use in react :
☢️. `UseState()` Hook
☢️. `UseRef` Hook
☢️. `UseMemo()` Hook
☢️. `UseEffect()` Hook


   1. **UseSate Hook Code :**

   ```Javascript
   import React, { useState } from 'react';
   function MyComponent() {
   const [myState, setMyState] = useState(initialValue);
   // Rest of your component logic
   return (
   // JSX rendering
   );
   }
   ```

   2. **UseRef Hook code :**

   ```Javascript
import React, { useRef, useEffect } from 'react';

function ExampleComponent() {
  // Creating a ref
  const myRef = useRef(null);

  useEffect(() => {
    // Accessing the current property of the ref
    console.log(myRef.current);

    // Performing some operation on the DOM element
    if (myRef.current) {
      myRef.current.focus();
    }
  }, []);

  return (
    <div>
      {/* Assigning the ref to an input element */}
      <input ref={myRef} type="text" />
    </div>
  );
}

export default ExampleComponent;





   ```

   3. **UseEffect Hook**

```Javascript
import React, { useEffect } from 'react';

function MyComponent() {
  useEffect(() => {
    // Your code for side effects goes here
    return () => {
      // Cleanup code (optional)
    };
  }, [/* dependencies */]);

  // Rest of your component code
}




```
**Another Example :**
**`Example 1:`** 
```Javascript
import React, { useState, useEffect } from 'react';

function DataFetchingComponent() {
  const [data, setData] = useState(null);

  useEffect(() => {
    const fetchData = async () => {
      const response = await fetch('https://api.example.com/data');
      const result = await response.json();
      setData(result);
    };

    fetchData();
  }, []); // Empty dependency array means it runs once after initial render

  return (
    <div>
      {/* Render the data */}
    </div>
  );
}


```

**`Example 2: `**
```Javascript
import React, { useState, useEffect } from 'react';

function SubscriptionComponent() {
  const [count, setCount] = useState(0);

  useEffect(() => {
    const intervalId = setInterval(() => {
      setCount((prevCount) => prevCount + 1);
    }, 1000);

    return () => {
      clearInterval(intervalId); // Cleanup function to clear the interval when component unmounts
    };
  }, []); // Empty dependency array means it runs once after initial render

  return (
    <div>
      <p>Count: {count}</p>
    </div>
  );
}

```


   4.  **UseMemo Hook Code :**

  ```Javascript
import React, { useMemo, useState } from 'react';

const ExampleComponent = ({ value }) => {
  const squaredValue = useMemo(() => {
    console.log("Expensive computation!");
    return value * value;
  }, [value]);

  return (
    <div>
      <p>Original Value: {value}</p>
      <p>Squared Value (Memoized): {squaredValue}</p>
    </div>
  );
};

const App = () => {
  const [inputValue, setInputValue] = useState(5);

  return (
    <div>
      <input
        type="number"
        value={inputValue}
        onChange={(e) => setInputValue(parseInt(e.target.value))}
      />
      <ExampleComponent value={inputValue} />
    </div>
  );
};

export default App;
      
  ```

## Aurthor :

**`NAME`** : **`KINSHUK JAIN `**
**`EMAIL`**: **`kinshuk25jan04@gmail.com`**


      

   
