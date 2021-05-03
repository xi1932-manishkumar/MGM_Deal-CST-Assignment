# Autocomplete multi-select

To create an autoselect, use the following element as reference:

<div class="autocomplete">
              <label for="project-name" style="display: none">Project Name</label>
              <br />
              <input type="text" placeholder="Project Name" name="project-name" id="project-name" class="ac"
                onclick="displayTitle(this, true)" />
</div>


Use the enclosing div with class "autocomplete" as a container

The label's for is set to the input's id, in this case "project-name"

Please note the class="ac", it is used to style the autocomplete elements and is required

# Selected values stored in object
There is a "selected" object within the script tags, which will have a property named with the first part of the element id (before the hyphen). This property will hold the current selected values for that input element.

const selected = {};

# Autocomplete watcher
To add autocomplete watcher to any element, add this to bottom of script:
autocomplete(document.getElementById("project-name"), countries);

where countries is the array of autocomplete suggestions
