---
defines-react-components: true 
---

```jsx:component:Clock

  const [time, setTime] = useState(new Date());

  useEffect(() => {
    const interval = setInterval(() => {
      setTime(new Date());
    }, 1000);
    return () => clearInterval(interval);
  }, []);

  const hours = time.getHours().toString().padStart(2, '0');
  const minutes = time.getMinutes().toString().padStart(2, '0');
  const seconds = time.getSeconds().toString().padStart(2, '0');

  const loadFont = () => {
    const link = document.createElement('link');
    link.href = 'https://fonts.googleapis.com/css2?family=Orbitron&display=swap';
    link.rel = 'stylesheet';
    document.head.appendChild(link);
  }

  useEffect(() => {
    loadFont();
  }, []);

  return (
  <div style={{
      fontFamily: 'Orbitron, monospace',
      fontSize: '4rem',
      textAlign: 'center',
      color: '#e4d6a7',
      backgroundColor: '#4d4d4d',
      padding: '1rem',
      borderRadius: '0.5rem',
      boxShadow: '0 0 0.5rem rgba(0, 0, 0, 0.5)'
    }}>
      {hours}:{minutes}:{seconds}
    </div>
  );

```
