# Tutorial: Debugging with Codezero

This project sets up a minimal HTTP server using Node.js. It listens for incoming requests, logs the user ID from the request headers, and forwards the requests to a specified service.

The best way to start the tutorial is by visiting <https://docs.codezero.io/tutorial>.

## Getting Started

### Prerequisites

- Node.js installed on your machine.

### Installation

1. Clone the repository:

   ```sh
   git clone https://github.com/c6o/tutorial-js
   ```

2. Navigate to the project directory:

   ```sh
   cd tutorial-js
   ```

### Running the Application

To start the server (and run service-b standalone), run:

```sh
npm start
```

The server will listen on port 8080, and your local copy of service-b will be processing requests from frontend app using your x-c6o-userid header.

### Debugging with Codezero

To run service-b locally and debug from within your preferred IDE, do the following:

1. Navigate to your [project_directory]/tutorial-js and run `czctl compose start` to serve your local variant of service B and consume all services in the tutorial namespace. (This command uses the [codezero-compose.yaml](./codezero-compose.yaml) to set up your Codezero environment.
1. Set a breakpoint in line 6 in [src/index.js](./src/index.js#L6).
1. Launch the debugger.
1. The next request will be stopped by the debugger, allowing you to inspect local variables or step through the code.

NOTE: If you can't run the service in your debugger, make sure you "npm stop" the service you might have already started above with "npm start" :) 

## Contributing

Feel free to submit issues or pull requests for improvements or bug fixes.
