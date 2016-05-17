# React TodoMVC Example

> React is a JavaScript library for creating user interfaces. Its core principles are declarative code, efficiency, and flexibility. Simply specify what your component looks like and React will keep it up-to-date when the underlying data changes.

> _[React - facebook.github.io/react](http://facebook.github.io/react)_


## Running the App

### Dependencies

* [Vagrant](https://www.vagrantup.com/downloads.html) or other Docker/Docker compose runtime environment.

    Note: The Vagrant box provided has a pre-configured
    Docker/Docker compose environment and is the supported model. This is to ensure a consistent development
    environment by keeping the host OS and docker versions identical across all contributors machines. The
    application should be able to be run natively on docker/docker-compose but be aware that you are on your
    own if you experience problems!`

### Steps for running the application

1. Fork this Repository on GitHub.

2. Open a Terminal:

        git clone git@github.com:<your-github-username>/todomvc.git
        cd todomvc
        vagrant up
        vagrant ssh
        cd todomvc
        docker build -t todomvc .
        docker run -ti --rm -p 8080:80 todomvc

3. Open your browser to http://localhost:8888 or http://192.168.70.4:8080



## Learning React

The [React getting started documentation](http://facebook.github.io/react/docs/getting-started.html) is a great way to get started.

Here are some links you may find helpful:

* [Documentation](http://facebook.github.io/react/docs/getting-started.html)
* [API Reference](http://facebook.github.io/react/docs/reference.html)
* [Blog](http://facebook.github.io/react/blog/)
* [React on GitHub](https://github.com/facebook/react)
* [Support](http://facebook.github.io/react/support.html)

Articles and guides from the community:

* [How is Facebook's React JavaScript library](http://www.quora.com/React-JS-Library/How-is-Facebooks-React-JavaScript-library)
* [React: Under the hood](http://www.quora.com/Pete-Hunt/Posts/React-Under-the-Hood)

Get help from other React users:

* [React on StackOverflow](http://stackoverflow.com/questions/tagged/reactjs)
* [Discussion Forum](https://discuss.reactjs.org/)

_If you have other helpful links to share, or find any of the links above no longer work, please [let us know](https://github.com/tastejs/todomvc/issues)._


## Running

The app is built with [JSX](http://facebook.github.io/react/docs/jsx-in-depth.html) and compiled at runtime for a lighter and more fun code reading experience. As stated in the link, JSX is not mandatory.

To run the app, spin up an HTTP server (e.g. `python -m SimpleHTTPServer`) and visit http://localhost/.../myexample/.
