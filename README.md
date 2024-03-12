# Geolocation Service

## Overview

The Geolocation Service package provides functions to interact with geolocation data, allowing you to retrieve coordinates based on an address and vice versa.

## Installation

You can install the Geolocation Service package via npm:

```bash
npm install geolocation-service
```

## Usage

### Importing the Module

```javascript
const { getGeolocation, getAddress } = require('geolocation-service');
```

### Getting Geolocation for an Address

```javascript
const address = "New York, USA";

getGeolocation(address)
    .then(coordinates => {
        console.log("Coordinates:", coordinates);
    })
    .catch(error => {
        console.error("Error:", error);
    });
```

### Getting Address for Geolocation Coordinates

```javascript
const latitude = 40.7128;
const longitude = -74.0060;

getAddress(latitude, longitude)
    .then(address => {
        console.log("Address:", address);
    })
    .catch(error => {
        console.error("Error:", error);
    });
```

## API

### `getGeolocation(address)`

Retrieves the geolocation coordinates (latitude and longitude) for a given address.

- `address` (string): The address for which to retrieve geolocation coordinates.

Returns a Promise that resolves to an object containing the latitude and longitude coordinates.

### `getAddress(latitude, longitude)`

Retrieves the address for given geolocation coordinates.

- `latitude` (number): The latitude coordinate.
- `longitude` (number): The longitude coordinate.

Returns a Promise that resolves to the address corresponding to the provided coordinates.

## Contributing

Contributions are welcome! For major changes, please open an issue first to discuss what you would like to change.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
