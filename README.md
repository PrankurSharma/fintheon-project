Thank you for visiting this project. This project is a part of selection process for SDE role at Fintheon.

Technical Skills used in this project: ReactJS(Frontend), NodeJS(Backend), Netlify(Frontend deployment), Render(Backend deployment)

Link to the depoyed website:
https://aqitracker.netlify.app/

There are a few third party libraries used in order to perform the desired functionalities:

1. Express: This NodeJS framework is used in the backend in order to connect it with front end. The API responses are cached using a library that uses express.

2. Axios: Axios is used both at front and back end. Back end axios fetches the data from the API if necessary using the url provided by the front end. Axios at front end is used for fetching the records from the backend for the given city. Since, there are different apis for cities, api url is different for every city. This url is passed from front end to back end using axios.

3. ChartJS and react-chartjs-2: These libraries are used in the front end in order to draw the graphs for the corresponding air constituents.

4. express-api-cache: This library is used at the back end in order for the server to create a cache. Cache is created on the server side and it stores the data for 2 hours. Data is refreshed after every two hours and new data is automatically taken from the api. The difference in the data fetching speeds can be seen from the Networks tab under Developer Tools option on the browser. Data is fetched much faster from the cache as compared to direct api fetching. Everytime a new record is fetched, it initially gets fetched from the api. Then, the api data is stored on the cache. When the data is requested again, it is fetched from the cache. 

Note: Please note that I have also implemented caching on the front end(using localStorage) and the code for that is commented out.  Steps are also mentioned in the code in order perform caching at front end. In that case, backend code will be commented out(mentioned in the code) and server folder will be useless in case of front end caching. Front end caching will delete the data stored in localStorage everytime the browser starts i.e. the data is stored in the localStorage till the browser in shut down.

5. CORS: Cors is another library that is used for seamless transfer of data between front end and back end. It provides a middleware for backend in order to communicate with front end.
