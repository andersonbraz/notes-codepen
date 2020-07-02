# Minhas Notas Codepen

Minhas anotações de configurações para Codepen.

## React + Bootstrap

Usando estilização com Bootstrap para teste ou prova de algum conceito com ReactJs.

### CSS

CSS Preprocessor = None

CSS Base = Neither

Vendor Prefixing = Neither

```shell
https://cdnjs.cloudflare.com/ajax/libs/twitter-bootstrap/4.5.0/css/bootstrap.min.css
https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.13.1/css/all.min.css
```

### Javascript

JavaScript Preprocessor = Babel

```shell
https://unpkg.com/react@16/umd/react.development.js
https://unpkg.com/react-dom@16/umd/react-dom.development.js
```

## React + Material

Usando estilização com Matrial para teste ou prova de algum conceito com ReactJs.

### CSS

CSS Preprocessor = None

CSS Base = Neither

Vendor Prefixing = Neither

```shell
https://cdnjs.cloudflare.com/ajax/libs/twitter-bootstrap/4.5.0/css/bootstrap.min.css
https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.13.1/css/all.min.css
```

### Javascript

JavaScript Preprocessor = Babel

```shell
https://unpkg.com/react@16/umd/react.development.js
https://unpkg.com/react-dom@16/umd/react-dom.development.js
```

## Bundle FreeCodeCamp

Para os exercícios do FreeCodeCamp lembrar de adicionar o seguinte Javascript:

```shell
https://cdn.freecodecamp.org/testable-projects-fcc/v1/bundle.js
```

## Estrutura

Exemplo de código para uma estrutura simples de aplicativo com ReacJs.

```javascript

const UserContext = React.createContext({
  username: 'andersonbraz',
  firstName: 'Anderson',
  lastName: 'Braz'
});

const UserConsumer = UserContext.Consumer;

class App extends React.Component {
  state = {
    user: {
      username: 'joaorossi',
      firstName: 'João',
      lastName: 'Rossi'
    }
  }

  render() {
    return(
      <div className="box">
        <User />
      </div>
    )
  }

}

const User = () => (
  <div>
    <UserProfile />
  </div>
)

const UserProfile = (props) => (
  <UserConsumer>
    {context => {
      return(
        <div>
          <div className="subtitle">Profile Page for</div>
          <h1 className="title">{context.username}</h1>
          <UserDetails />
        </div>
      )
    }}
  </UserConsumer>
)

const UserDetails = () => (
  <div>
    <UserConsumer>
      {context => {
        return (
          <div>
            <p><b>Username:</b> {context.username}</p>
            <p><b>First Name:</b> {context.firstName}</p>
            <p><b>Last Name:</b> {context.lastName}</p>
          </div>
        )
      }}
    </UserConsumer>
  </div>
)

ReactDOM.render(<App />, document.getElementById("root"));
```
