# Web Copter

A quadcopter controlled with custom elements and JavaScript.
This is a prototype project meant to show how web components (and more specifically custom elements) can be used
to build a hardware application. The quadcopter is very rudimentary and a work in progress.

## Preview

Web components let you build applications declaratively, which can make them easier to understand, grow, and maintain. Here is some of the main HTML source code of the quadcopter:

```
<jfive-motor on="[[motorOn1]]" speed="[[speed1]]" reverse="[[reverse1]]" pwm-pin="GPIO12" dir-pin="GPIO23" cdir-pin="GPIO24"></jfive-motor>
<jfive-motor on="[[motorOn2]]" speed="[[speed2]]" reverse="[[reverse2]]" pwm-pin="GPIO18" dir-pin="GPIO20" cdir-pin="GPIO21"></jfive-motor>
<jfive-motor on="[[motorOn3]]" speed="[[speed3]]" reverse="[[reverse3]]" pwm-pin="GPIO13" dir-pin="GPIO27" cdir-pin="GPIO22"></jfive-motor>
<jfive-motor on="[[motorOn4]]" speed="[[speed4]]" reverse="[[reverse4]]" pwm-pin="GPIO19" dir-pin="GPIO6" cdir-pin="GPIO5"></jfive-motor>
```

Even if you have never built hardware before, I'll bet you already know the most important things going on in the code above. That's one of the powers of declarative programming.

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

From your Raspberry Pi, and from the `web-copter` directory:
```
sudo su
npm start
```

An HTTP server will now be running from your Raspberry Pi. Go to your Pi's IP address with port 5000 to access the web quadcopter controls.
