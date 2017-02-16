# Web Copter

A quadcopter controlled with custom elements and JavaScript.
This is a prototype project meant to show how web components (and more specifically custom elements) can be used
to build a hardware application. The quadcopter does not fly, but the four motors can be controlled (and you can imagine it is flying).

## Preview

Web components let you build applications declaratively, which can make them easier to understand, grow, and maintain. Here is the main HTML source code of the quadcopter:

```
```

Even if you have never built hardware before, I'll bet you already know the most important things going on in the code above.

## Installation

Right now this project has only been tested on a Raspberry Pi Model 3 B. It will be portable to other boards in the future.

From your Raspberry Pi:
```
git clone https://github.com/scramjs/web-copter.git
cd web-copter
bower install
npm install
npm run rebuild
```

Don't worry, Bower will be going away soon. I'm just waiting on Polymer to officially support NPM.

## Use

From your Raspberry Pi, from the `web-copter` directory:
```
sudo su
npm start
```

An HTTP server will now be running from your Raspberry Pi. Go to your Pi's IP address with port 5000 to access the web quadcopter controls.
