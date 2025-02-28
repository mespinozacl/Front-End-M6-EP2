# Front-End-M6-EP2
----
npm create vite@latest
cd m6-ep1
npm install typescript ts-loader webpack webpack-cli --save-dev
npm install react-router-dom
npm install axios
npm install crypto-js
npm i --save-dev @types/crypto-js
npm install use-debounce
npm install json-server
npm run server
npm run dev

npm install vite-plugin-pwa --save-dev

----
1. Uso de LocalStorage
EquipoMedico.tsx
...
  let searchTermLocal = localStorage.getItem('searchTerm');
  const [searchTerm, setSearchTerm] = useState(searchTermLocal ? searchTermLocal:'');
...
  onChange={(e) => {filterBySpec(e.target.value); localStorage.setItem('searchTerm', e.target.value);} }

2. Uso de IndexedDB
Dashboard.tsx (DashboardBD)
-> se almacena los registros secure-data
-> se puede controlar dejando offline el servidor que alimenta los datos protegidos (npm run server)

EquipoMedico.tsx (EquipoMedicoBD)
-> se almacenan los registros que se obtienen de la api de doctores simulada (externa con otros datos)

3. Se verifica con Dashboard, funciona offline 
   Se verifica con EquipoMedico, funciona offline 

4. Se obtienen informes satisfactorios de acuerdo a lo solicitado