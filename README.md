# Flask Weather Data API

The provided code sets up a Flask web application that serves a Weather Data API. It uses the Flask framework to create routes that handle different API endpoints and render an HTML template for the home page.

## Routes

- **Home**: The root route ("/") renders the "home.html" template and passes the stations data as HTML to be displayed on the page.

- **Single Date Data**: The route ("/api/v1/<station>/<date>") accepts a station ID and a date as parameters. It reads the corresponding data file and retrieves the temperature value for the specified date and station. It returns a JSON response containing the station ID, date, and temperature.

- **All Data for Station**: The route ("/api/v1/<station>") accepts a station ID as a parameter. It reads the data file for the specified station and returns all the data for that station in JSON format.

- **Yearly Data for Station**: The route ("/api/v1/yearly/<station>/<year>") accepts a station ID and a year as parameters. It reads the data file for the specified station and filters the data to include only the records for the specified year. It returns the filtered data in JSON format.

## HTML Template

The "home.html" template is rendered for the home route ("/"). It provides some information about the API and displays the stations data in a table. The stations data is passed to the template as an HTML string using the `data` variable.

## Running the Application

To run the Flask application:

1. Ensure you have installed the required dependencies by running `pip install -r requirements.txt` in your terminal or command prompt.
2. Make sure you have the necessary data files in the correct format (e.g., "data_small/stations.txt", "data_small/TG_STAID<station_id>.txt").
3. Execute the `main.py` script using Python: `python main.py`.
4. The Flask application will start running, and you should see output indicating that the server is running on "http://127.0.0.1:5000/".
5. Open your web browser and navigate to "http://127.0.0.1:5000/" to access the home page and explore the API endpoints.

Please note that the application is currently running in debug mode (`debug=True`). This mode enables automatic reloading of the server when changes are made to the code. In a production environment, you should disable debug mode by setting `debug=False` in the `app.run()` call.

That's it! You now have a Flask web application that serves a Weather Data API. Feel free to customize the routes, add more functionality, or enhance the HTML template to suit your needs. Happy coding!

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more information.

## Acknowledgement

This code is based on the work by Ardit Sulce and is used with permission. The original code can be found at this [link](https://github.com/arditsulceteaching/mega-course-app6-weather-api.git).
