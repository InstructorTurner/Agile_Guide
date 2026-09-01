# ⚛️ React Cheat Sheet

## 🚀 Essential Hooks
| Hook | Purpose | Example |
| :--- | :--- | :--- |
| `useState` | Manage local state | `const [count, setCount] = useState(0);` |
| `useEffect` | Side effects (API calls, timers) | `useEffect(() => { ... }, [dependency]);` |
| `useContext` | Global state without prop drilling | `const theme = useContext(ThemeContext);` |
| `useRef` | Direct DOM access / persistent value | `const inputRef = useRef(null);` |
| `useMemo` | Memoize expensive calculations | `const val = useMemo(() => compute(), [dep]);` |
| `useCallback` | Memoize function definitions | `const fn = useCallback(() => { ... }, [dep]);` |

## 🧩 Component Patterns
### Functional Component
```jsx
import React from 'react';

const UserProfile = ({ user }) => {
  return (
    <div>
      <h1>{user.name}</h1>
      <p>{user.email}</p>
    </div>
  );
};

export default UserProfile;
```

### Conditional Rendering
```jsx
{isLoggedIn ? <LogoutButton /> : <LoginButton />}
{items.length > 0 && <ItemList items={items} />}
```

### Mapping Lists
```jsx
<ul>
  {items.map(item => (
    <li key={item.id}>{item.name}</li>
  ))}
</ul>
```

## 🛠️ Common Gotchas
*   **Key Prop:** Always provide a unique `key` when mapping lists to avoid rendering bugs.
*   **State Async:** `setState` is asynchronous. Use the functional update `setCount(prev => prev + 1)` for updates based on previous state.
*   **Effect Loop:** Always define the dependency array in `useEffect` to prevent infinite re-renders.
