# Serverless with IBM Cloud Functions: Codelab

## Your first Action, Trigger, and Sequence

1. Create action current-time.js

`function main(params) {
    var date = new Date();
    return { message:
"Invoked at: " + date.toLocaleString(),
	    time: date.toLocaleString()
	};
}`

2. Create action random-number.js

`function main(params) {
	return { value: Math.floor(Math.random()*900000),
	        time: params.time};
}`

3. Create action message.js

`function main(params) {
	return { message: 'Generated ' + params.value + ' at ' + params.time };
}`

4. Create enclosing sequence for all 3 actions ‘sequence’

5. Create periodic trigger every-5-seconds

`*/5 * * * * *`

---

## Serverless HTTP REST Endpoints
