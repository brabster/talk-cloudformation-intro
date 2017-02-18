## Nested Stacks

CloudFormation's way of reusing and composing stacks

<section>
<div style="float: left; margin: 5px">
    <img src="images/minibricks/pile.jpg" height="300"></img>
    <p>AWS Resources</p>
</div>

<div class="fragment" style="float: left; margin: 5px">
    <img src="images/minibricks/part.jpg" height="300"></img>
    <p>Nested Stacks</p>
</div>

<div class="fragment" style="float: left; margin: 5px">
    <img src="images/minibricks/r2d2.jpg" height="300">
    <p>R2D2!<span class="fragment" style="float: right;">(Products)</span></p>
</div>
</section>

Note:
- The bricks represent individual AWS resources, like load balancers, DynamoDB tables, Lambda functions, Kinesis Streams. Working at this level of abstraction gets harder as the number of resources increases.
- Nested stacks allow multiple resources to be composed into more manageable units, like a message deduplicator or image thumbnailer.
- Add nesting as needed to solve your problems manageably!
