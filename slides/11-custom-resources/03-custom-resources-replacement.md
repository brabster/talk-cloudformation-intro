## Custom Resources

Updates may "replace" resources!

![Custom resource messaging](images/custom-resources/custom-resources-messaging-replacement.svg)

Replace = create new then delete old

Note:
 - We are imagining that our Pingdom Ping cannot be modified and must be replaced
 - Also applies to normal resources; an update requiring a replacement will create a new resource then delete the old one
 - Which is why custom names are a problem - often cannot create another resource with the same name!
 - Force an effective replacement by changing the logical resource ID in the template

