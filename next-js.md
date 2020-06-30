Init app
```bash
npx create-next-app app-name
```

CSS in Next
```jsx
<style jsx>{`
  h1 {
    color: #30475e:
  }
`}</style>
```

Use emotion styled components
```json
{
  "presets": [
    "next/babel",
    "@emotion/babel-preset-css-prop"
  ],
  "plugins": [
    [
      "emotion"
    ]
  ]
}
```
Usage
```jsx
import styled from '@emotion/styled';

const Heading = styled.h1`
  color: #c70039:
`;

const Home = () => (
  <div>
    <Heading>Home</Heading>
  </div>
);
```

Routing
```jsx
import Link from 'next/link';

<Link href="/">Home</Link>
<Link href="/contact">Contact</Link>
```
