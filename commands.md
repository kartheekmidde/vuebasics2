<h2>Basic info and commands</h2>
<ul>
    <li> 
        To create new project -         
        <code>
            vue create projectname
        </code>
    </li>
    <li> 
        Script to spin a local development server -         
        <code>
            npm run serve
        </code>
        or
        <code>
            vue-cli-service serve
        </code>
    </li>
    <li> 
        Template reference - <br>add ref="name" and then refer using this.$refs.name
    </li>
    <li> 
        Using one component in another - 
        <br>1. Create the new component.
        <br>2. Import the new component in parent component and declare in the exports.
        <br>3. Use the new component in template of the parent component.
    </li>
    <li> 
        To limit CSS to that component add <code>scoped</code> to style
    </li>
    <li> 
        To pass data to other component, use <code>props</code> as array and/or do data binding. Props are optional.
    </li>
    <li> 
        To pass simple data from child to parent component, use <code>Event listeners - this.$emit('eventName')</code>. In the parent component use <code>@eventName=""</code> as listener.
    </li>
    <li> 
        To have event modifiers, use <code>@click.eventModifier</code>.
    </li>
    <li> 
        To pass templates, use <code>slots or named slots</code>. Dont use slots for simple data and we cant use self closing component template. To use named slots define a template with <code>v-slot:templName</code> and use slot with name property. We can pass default content as well.
    </li>
    
</ul>
