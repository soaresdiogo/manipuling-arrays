## TIPS to manipulate arrays

```
const data = [
    { brand: "Apple", model: "Macbook", price: 2200, isNew: true },
    { brand: "Dell", model: "Gaming", price: 1348, isNew: true },
    { brand: "Lenovo", model: "ThinkPad", price: 500, isNew: false },
    { brand: "Avell", model: "A65", price: 1200, isNew: false },
    { brand: "HP", model: "Pavillion", price: 1499, isNew: true }
  ];
```
#### REVERSE - it reverses the original array
```
  const dataReverse = data.reverse();
  console.log("original", data);
  console.log("reversed", dataReverse);

  /* You can use unstructure the original object */

  const dataReverseUnstructure = [...data].reverse();
  console.log('original', data);
  console.log('Reversed unstructure', dataReverseUnstructure);
```

#### FIND - it find anything inside array depending of logical and stop the search after found the first element
```
  const laptopDell = data.find((item) => {
    return item.brand === 'Dell';
  });
  console.log('find', laptopDell);
```
#### FINDINDEX - it return the index position of element found in array 
```
  const modelGaming = data.findIndex((item) => {
    return item.model === 'Gaming';
  });
  console.log('findIndex', modelGaming);
```
#### INCLUDES - it verify if exists an alement in array and it return a boolean 
```
  const brands = ["Apple", "Dell", "Avell", "Lenovo", "HP"];
  const hasAvell = brands.includes("Avell");
  console.log('includes', hasAvell);
```
#### MAP - it return a new object modified depending of logical applyed, it does a looping over original array like  "for", but retuning a new object

   ```
  const handleSetAllToUsedLaptops = data.map(item => {
    item.isNew = false;
    return item;
  });
  console.log('map', handleSetAllToUsedLaptops);
```

#### FILTER - it return all elements depending of logical. The difference between FIND and FILTER is that FIND stop when it found the first element and the FILTER go through the entire list, and both return a new array
   ```
  const newLaptops = data.filter(item => item.isNew);
  console.log('FILTER', newLaptops);
```
#### REDUCE - returns a value or an object depending on the logic and it groups the values being able to add and get a total value for example
   ```
  const totalProducts = data.reduce((total, item) => {
    return total += item.price;
  }, 0);
  console.log('REDUCE', totalProducts);
```
#### FOREACH - it interate with list
```
  data.forEach(item => {
    console.log(`Laptop brand: ${item.brand}`);
  });
```
#### SOME - it verify if anything corresponding with the value that I'm wanting, it return a boolean
   ```
  const hasUsedLaptops = data.some((item) => !item.isNew);
  console.log("SOME", hasUsedLaptops);
```
#### EVERY - it verify if all element containt a value, it return a boolean
   ```
  const everyLaptopsHasPrice = data.every(item => item.price);
  console.log(everyLaptopsHasPrice);
```
#### AT - it return an object according to position of array, beigin that if you put -1, it return the last element
   ```
  const lastElement = data.at(-1);
  console.log(lastElement);
```
