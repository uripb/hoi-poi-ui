Horizontal label:

```jsx
let state = state || {};
const onChange = (field) => {
    return (e) => {
        setState({ [field]: e && e.target ? e.target.value : '' });
    };
};

<div>
    <Input label="Lorem ipsum" placeholder="Write here" onChange={onChange(1)} value={state[1]} />
    <Input
        label="Lorem ipsum"
        placeholder="Write here"
        hint="Hello!"
        isRequired
        onChange={onChange(2)}
        value={state[2]}
    />
    <Input
        label="Lorem ipsum Lorem ipsum Lorem ipsum"
        placeholder="Write here"
        hint="Hello!"
        isRequired
        onChange={onChange(3)}
        value={state[3]}
    />
    <Input label="Lorem ipsum" placeholder="Write here" error="I am an error" />
    <Input label="Lorem ipsum" placeholder="Write here" value="I am disabled" isReadOnly={true} />
</div>;
```

Vertical label:

```jsx
const onChange = (e) => setState({ value: e && e.target ? e.target.value : '' });
<div>
    <Input
        label="Lorem ipsum"
        labelMode="vertical"
        placeholder="Write here"
        onChange={onChange}
        value={state.value}
    />
</div>;
```

Pre/Post components

```jsx
import { Icon } from 'hoi-poi-ui';
const onChange = (e) => setState({ value: e && e.target ? e.target.value : '' });
<div>
    <Input
        label="Lorem ipsum"
        placeholder="Write here"
        onChange={onChange}
        value={state.value}
        preComponent={<span>$</span>}
        postComponent={<Icon name="chevron" />}
    />
</div>;
```

### Component tree

---

-   input - Native input
-   error - Error wrapper
-   formControl - Input wrapper excluding label
-   [Label](#/Forms?id=label)
-   preComponent - Component rendered at the input beginning
-   postComponent - Component rendered at the input ending
