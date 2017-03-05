## Nested Stack Performance Tip

Prefer wide and shallow, not narrow and deep!

<section>
  <img width="400" style="vertical-align: top; margin: 1em" src="images/nested-stacks/shallow.dot.svg"/>
  <img height="400" style="margin: 1em" src="images/nested-stacks/deep.dot.svg"/>
</section>

Note:
- Deeply nested resources will take longer to update than shallowly nesteds
- Messages will be sent in parallel for sub-resources of a single resource.
- Messaging pattern affect by nested stack structure, cross-references and explicit DependsOn parameters.
