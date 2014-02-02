# AAF Rapid Connect - Python Sample App

In addition to the information and live demo available from the [Rapid Connect page](http://rapid.aaf.edu.au), we have provided the following sample code which underpins our examples.

This is the Python sample application. It is provided purely for illustrative purposes only to give you an idea of how we went about building our Python demo. It should be noted that the code presented here should not be used as a base to build your application, but is provided to give you an idea of the concepts behind connecting a service so you can pick it apart (everybody’s requirements are different and just cutting and pasting the code won’t generally work if you decide to do that). No effort has been made to audit the code's security, or make it production-ready.

AAF has used the Google App Engine SDK, and the webapp2 framework to develop this application. It is a prerequisite of this sample application that you are able to run Google App Engine applications. Please see the [Google App Engine](https://developers.google.com/appengine/) developer's guide for more information. As this is purely for illustrative purposes, AAF is regretfully unable to provide support for the webapp2 framework and general Google App Engine or Python development questions, you will need to get in touch with your local software development team to help you out here :smile:.

## Getting Started

There are three modifications which **MUST** be made before this application will work correctly:

1. In `main.py`, replace the `secret_key` with a new, random value that you have generated. Keep it secret.
2. In `main.py`, replace the value of `jwt_secret` with a new, random value that you have generated. This will be your **Secret** which is used during registration with Rapid Connect.
3. In `views/index.html`, find the link with `href="INSERT_YOUR_RAPID_CONNECT_URL_HERE"`. Replace the value of the `href` with the **UNIQUE URL** provided after you register your application.

### Registration

You may register against [Rapid Connect Test](http://rapid.test.aaf.edu.au) to test this application. Please use a sensible descriptive name for your service. It's much easier for us if we don't have a database full of "test service" belonging to various people.

If you are running this on your desktop with the default settings, the callback URL is most likely `http://localhost:8080/auth/jwt`

### Starting the application

On Linux, Mac OS X and other UNIX-like operating systems, the following command will start the application:

    dev_appserver.py app.yaml

If you encounter any errors, please review the [Google App Engine](https://developers.google.com/appengine/) developer's guide to ensure you have completed all the necesssary setup.

## License

Copyright 2014, Australian Access Federation

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

### Contributing

AAF is happy to accept contributions which improve the quality of this sample application. Feel free to issue a pull request.
