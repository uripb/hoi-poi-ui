**Schema:**

```jsx
const schema = [
    {
        title: 'General', // Section title
        fields: [
            {
                label: 'Email',
                labelMode: 'horizontal', // Override general labelMode
                isFullWidth: false, // Override general isFullwidth
                name: 'email',
                type: 'text', // text|inputGroup|checkboxGroup|radioGroup|select|slider
                placeholder: 'Your email',
                hint: 'No spam!',
                isReadOnly: true,
                isRequired: true,
                attrs: {}, // Rest of props passed directly to field
            },
        ],
    },
];

return <pre>{JSON.stringify(schema, null, 4)}</pre>;
```

**Types:**

```jsx
const types = ['text', 'inputGroup', 'checkboxGroup', 'radioGroup', 'select', 'slider'];

return <pre>{JSON.stringify(types, null, 4)}</pre>;
```

```jsx
import schema from './example.json';

const errors = {
    phone: 'Invalid phone',
};

let onChange = (values, field) => setState({ values });
<Form onChange={onChange} values={state.values} errors={errors} schema={schema} />;
```

### Component tree

---

-   form - native form element
-   [Section](#/Forms?id=Section)
