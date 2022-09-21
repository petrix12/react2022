# Crea tu primer proyecto en react
+ URL: https://www.udemy.com/course/crea-tu-primer-proyecto-en-react-js
+ Autor: Angelo Parra

## Contenido del curso
### Sección 1: Introdcción
#### 1. Introducción
+ Extensión de VSC recomenda:
    + ES7 React/Redux/GraphQL/React-Native snippets
        + rodrigovallades


### Sección 2: Creando el proyecto con create-react-app
#### 2. Create-react-app
+ Página oficial de React.js: https://reactjs.org
1. Crear proyecto React.js:
    + $ npx create-react-app galery
2. Iniciar proyecto:
    + $ cd galery
    + $ npm start

### Sección 3: Limpiando el proyecto
#### 3. Limpiando el contenido de ejemplo
1. Modificar el **index.js** (galery\src\index.js):
    ```js
    import React from 'react';
    import ReactDOM from 'react-dom/client';
    import './index.css';
    import App from './App';

    const root = ReactDOM.createRoot(document.getElementById('root'));
    root.render(
        <React.StrictMode>
            <App />
        </React.StrictMode>
    );
    ```
2. Modificar el componente principal **App.js** (galery\src\App.js):
    ```js
    import './App.css';

    function App() {
        return (
            <div className="App">
            <h1>Soluciones++</h1>
            </div>
        );
    }

    export default App;
    ```
3. Modificar el archivo de estilo **index.css** (galery\src\index.css):
    ```js
    /* Dejar en blanco */
    ```
4. Modificar el **App.css** (galery\src\App.css):
    ```css
    /* Dejar en blanco */
    ```

### Sección 4: Creando componentes
#### 4. Creacion de los componentes del proyecto
+ **Atajo para crear componentes React**: rafce
1. Crear componente **Aurora** (galery\src\components\Aurora.js):
    ```js
    import React from 'react'
    import AuroraImg from '../images/aurora.jpg'

    const Aurora = () => {
        return (
            <div>
                <img src={AuroraImg} alt="" />
            </div>
        )
    }

    export default Aurora
    ```
2. Crear componente **Beach** (galery\src\components\Beach.js):
    ```js
    import React from 'react'
    import BeachImg from '../images/beach.jpg'

    const Beach = () => {
        return (
            <div>
                <img src={BeachImg} alt="" />
            </div>
        )
    }

    export default Beach
    ```
3. Crear componente **Forest** (galery\src\components\Forest.js):
    ```js
    import React from 'react'
    import ForestImg from '../images/forest.jpg'

    const Forest = () => {
        return (
            <div>
                <img src={ForestImg} alt="" />
            </div>
        )
    }

    export default Forest
    ```
4. Crear componente **Jungle** (galery\src\components\Jungle.js):
    ```js
    import React from 'react'
    import JungleImg from '../images/jungle.jpg'

    const Jungle = () => {
        return (
            <div>
                <img src={JungleImg} alt="" />
            </div>
        )
    }

    export default Jungle
    ```
5. Crear componente **Lake** (galery\src\components\Lake.js):
    ```js
    import React from 'react'
    import LakeImg from '../images/lake.jpg'

    const Lake = () => {
        return (
            <div>
                <img src={LakeImg} alt="" />
            </div>
        )
    }

    export default Lake
    ```
6. Crear componente **Milky** (galery\src\components\Milky.js):
    ```js
    import React from 'react'
    import MilkyImg from '../images/milky.jpg'

    const Milky = () => {
        return (
            <div>
                <img src={MilkyImg} alt="" />
            </div>
        )
    }

    export default Milky
    ```

### Sección 5: Navegación
#### 5. creando la navegacion
+ https://www.npmjs.com/package/react-router-dom
1. Instalar dependencia **React Router DOM**:
    + $ npm i react-router-dom

### Sección 6: Concluyendo la navegación
#### 6. Completando la navegacion
1. Modificar componente padre **App** (galery\src\App.js):
    ```js
    import './App.css';
    import { BrowserRouter as Router, Route } from "react-router-dom";
    import Aurora from './components/Aurora';
    import Beach from './components/Beach';
    import Forest from './components/Forest';
    import Jungle from './components/Jungle';
    import Lake from './components/Lake';
    import Milky from './components/Milky';
    import Navegacion from './components/Navegacion';

    function App() {
        return (
            <Router>
                <Route path='/aurora' component={Aurora} />
                <Route path='/beach' component={Beach} />
                <Route path='/forest' component={Forest} />
                <Route path='/jungle' component={Jungle} />
                <Route path='/lake' component={Lake} />
                <Route path='/milky' component={Milky} />
                <Navegacion />
            </Router>
        );
    }

    export default App;
    ```
2. Crear componente **Navegacion** (galery\src\components\Navegacion.js):
    ```js
    import React from 'react'
    import { Link } from "react-router-dom"
    import AuroraImg from '../images/aurora.jpg'
    import BeachImg from '../images/beach.jpg'
    import ForestImg from '../images/forest.jpg'
    import JungleImg from '../images/jungle.jpg'
    import LakeImg from '../images/lake.jpg'
    import MilkyImg from '../images/milky.jpg'

    const Navegacion = () => {
        return (
            <div>
                <Link to="/aurora">
                    <figure>
                        <img src={AuroraImg} alt="" />
                        <figcaption>Aurora</figcaption>
                    </figure>
                </Link>
                <Link to="/beach">
                    <figure>
                        <img src={BeachImg} alt="" />
                        <figcaption>Beach</figcaption>
                    </figure>
                </Link>
                <Link to="/forest">
                    <figure>
                        <img src={ForestImg} alt="" />
                        <figcaption>Forest</figcaption>
                    </figure>
                </Link>
                <Link to="/jungle">
                    <figure>
                        <img src={JungleImg} alt="" />
                        <figcaption>Jungle</figcaption>
                    </figure>
                </Link>
                <Link to="/lake">
                    <figure>
                        <img src={LakeImg} alt="" />
                        <figcaption>Lake</figcaption>
                    </figure>
                </Link>
                <Link to="/milky">
                    <figure>
                        <img src={MilkyImg} alt="" />
                        <figcaption>Milky</figcaption>
                    </figure>
                </Link>
            </div>
        )
    }

    export default Navegacion
    ```

### Sección 7: Agregando estilos
#### 7. Agregando estilos al proyecto
+ https://getbootstrap.com
1. Agregar los estilos de bootstrap mediante CDN en **galery\public\index.html**.
2. Modificar **galery\src\components\Navegacion.js**:
    ```js
    ```
3. mmmm



    ```js
    ```

### Sección 8: Final de la primera parte
#### 8. Final de estilos y galeria completa



#### 9. Inscribete al curso completo
