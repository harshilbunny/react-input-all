# react-input-all

> React input is a lightweight, dependency free component for building forms in React without having to think about what happens under the hood. It uses one component and an array of objects that describe the inputs in the form.

[![NPM](https://img.shields.io/npm/v/react-input-all.svg)](https://www.npmjs.com/package/react-input-all) [![JavaScript Style Guide](https://img.shields.io/badge/code_style-standard-brightgreen.svg)](https://standardjs.com)

## Install

```bash
npm install --save react-input-all
```

## Usage

```jsx
import React, { useState } from "react";
import AllInput from 'react-input-all'
import 'react-input-all/dist/index.css'

const MyComponent = () => {
  const [form, setForm] = useState([
    { name: 'name', value: '', placeholder: 'Write Your Name' },
    { name: 'email', value: '', placeholder: 'Write Your Email' },
    { name: 'phone', value: '', placeholder: 'Write Your Phone No.' }
  ])
  const onBlurChange = (e, index) => {
    let value = e.target.value
    console.log('form data:>> ', form[index], 'event=>', e);

  }
  const handleChange = (e, index) => {
    let value = e.target.value
    console.log('form data:>> ', form[index], 'event=>', e);
  }
  return (
    <AllInput
      form_fields={form}
      onBlurChange={onBlurChange}
      handleChange={handleChange}
    />
  )
}

export default MyComponent
```

## License

MIT © [harshilbunny](https://github.com/harshilbunny)
