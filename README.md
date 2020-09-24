## My learnings from this project

### using middlewares

### throwing error using throw new Error('Slug in use. 🍔')

### validating schema using yup

### setting static folder path using express
app.use(express.static('./public'));

### Returns middleware that only parses json
app.use(express.json());

### express rate limit :
https://www.youtube.com/watch?v=mZ0O7gcS7Yk

### path.join
The path.join() method joins all given path segments together using the platform-specific separator as a delimiter, then normalizes the resulting path.

The __dirname in a node script returns the path of the folder where the current JavaScript file resides

const notFoundPath = path.join(__dirname, 'public/404.html');

### dotenv 
https://www.youtube.com/watch?v=5WFyhsnU4Ik

### morgan
morgan is a  logging tool that anyone who works with HTTP servers in Node.js should learn to use. morgan is a middleware that allows us to easily log requests, errors, and more to the console. It’s easy to use, but still powerful and customizable.

### helmet 
helps in security of api..one of the usecase is that it helps the so unsecure
info is not present in response headers on hitting curl command 
https://www.youtube.com/watch?v=tGMPWVl_l9Y

### Rate Limiting your endpoints
Let's face it. Not everybody in the world has best intentions for your architecture. Sure, attacks like DDoS are simply very complicated to mitigate, and even giants like GitHub go down when something like that happens.

But the least you can do is prevent a script-kiddie from taking down your server just because you have an expensive API endpoint exposed from your server without any rate-limiting in place.

If you use Express with Node, there are 2 beautiful packages which work seamlessly together to rate limit traffic on Layer 7:

Express Rate Limit - https://www.npmjs.com/package/express-rate-limit
Express Slow Down - https://www.npmjs.com/package/express-slow-down

Express Slow Down actually adds incremental delay to your requests instead of dropping them. This way legit users, if they DDoS by accident (super activity of clicking buttons here and there), are simply slowed down and are not rate limited.

On the other hand, if there's a script-kiddie running scripts to take down the server, Express rate limiter monitors and rate limits that particular user, depending on the user IP, user account, or anything else you want.

Rate limiting could (should!) be applied on Layer 4 as well (Layer 4 means blocking traffic before discovering the contents of it - HTTP) through IP address. If you want, you can setup an NGiNX rule which blocks traffic on layer 4 and rejects the flood of traffic coming from a single IP, thus saving your server processes from overwhelming.


### notes while taking course
npm init -y
npm i express yup monk helmet morgan cors dotenv nodemon nanoid
require is used in Nodejs
app.get
app.listen
const port = process.env.port || 1337
scripts creation in package.json concept
setup static folder using express
"* {
margin : 0
padding : 0
box-sizing : border-box
}"
npm now config ...check it out
netlify..horoku...aws...hosting providers
namecheap.com : // update cname

creating schema using yup
using mock to connect wd mongo database
creating index on mongo using node
make index using in mongo
JSON.stringify
async await used together