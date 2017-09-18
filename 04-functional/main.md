# FUNCTIONAL

I don't know, whatever, think of functional programming as this

## no side effects
  - Side effects are things that happen outside of your function call

  ```js
  // don't do this
  const bands = {
    artist: 'LCD Soundsystem';
  }

  const changeName = () => {
    bands.artist = 'Yeah Yeah Yeahs';
  }

  // instead do something like this
  const changeName = (obj) => {
    return obj.artist = 'Yeah Yeah Yeahs';
  }

  // what about for any name?
  const changeName = (obj, name) => {
    return obj.artist = name;
  }

  // but you could generalize it even more
  const changeName = (obj, otherObject) => {
    return Object.assign(obj, otherObject);
  }
  ```
  - Some array methods also mutate your (ノ°Д°）ノ︵ ɐʇɐp, even if you try to not have side effects

  ```js
  const dataSet = [1, 2, 3, 4];

  const removeFirst = (data) => {
    data.shift();
    return data;
  };

  // calling data.shift(); will remove 1 from dataSet but check out what happened to dataSet itself. What can you do about this?

  // your first thought might be this, but why doesn't this work?
  const removeFirst = (data) => {
    let tmp = data.shift();
    return tmp;
  };

  // what about using filter instead?
  const removeFirst = (data) => {
    let temp = data.filter((item, i) => {
      if (i !== 0) {
        return item;
      }
    })

    return temp;
  };

  // I guess this feels a bit contrived but imagine a situation where you might accidentally change something but didn't intend to and have to track it down.
  ```
  - Here's a short list of array methods that are mutating, read more about it [here](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/prototype#Mutator_methods).
    - copyWithin
    - fill
    - pop
    - push
    - reverse
    - shift
    - sort
    - splice
    - unshift



I like to think of it as a way of generalizing the code that you write in a way so that you can reuse it. Think of it as building a toolset for tools. Functional programming lends itself to readability, consistency, and reuseable code.

What else.

## consistency
  - The code you write should consistently return the same output for the same input. In a lot of ways if you code doesn't rely on any outside forces or changing state it should always return the same thing.

  ```js
    const add = (n1, n2) => {
      return n1 + n2;
    }
  ```

  - This consistency allows you unit test your code with 100% reliability, I mean it would be pretty weird if 1 + 1 didn't equal 2, maybe it'll happen one day.

- This is nice and all but it can be pretty impractical sometimes if you adhere to this 100%, I personally think if you scope the idea of functional programming to the concept of consistency and no side effects, you'll be fine.

## practice
