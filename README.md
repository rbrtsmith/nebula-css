# rwsmith-grid
Probably the most feature packed and powerful responsive grid system you've 
ever come across&hellip;

##Features
* Fluid
* Infinitely nestable
* Optional equal height grid items based on flexbox (IE10+)
* Optional vertical alignment of grid items (when heights differ).
* Optional vertical gutters&mdash;which match the width of horizontal gutters.
* Large, standard, small or zero gutters&mdash;all of which are customizable.
* Ability to reverse the horizontal order of grid-items.
* No clearfixing required, rows of items with uneven heights tile gracefully.
* Based on fractions rather than columns yielding increased flexibility over
  some more traditional approaches that use a fixed number of columns.
* Intuitive class names based on a BEM methodology hybrid known as [BEMIT](http://csswizardry.com/2015/08/bemit-taking-the-bem-naming-convention-a-step-further/#responsive-suffixes)
* Does not require a wrapping element like most other grid systems.
* Extremely lightweight, using Sass @if blocks you can include only the
  features that you require via the `Feature-toggle` list.
* Width, push and pull classes are not tied directly to the grid, and can be 
  reused anywhere in your project.
* Ability to use any number of user-defined breakpoints with user defined
  namespaces to match.

##Demo
Coming soon!

##Setup
###Vars
Either roll with the defaults or simply adjust the values wherever necessary&hellip;
* `object-ns` set the object namespace e.g. `.[value]grid` &nbsp; `.[value]grid__item` 
 The default value is `o-` which gives `.o-grid` &nbsp; `.o-grid__item`
* `utility-ns` set the utility namespace e.g. `.[value]1/2` &nbsp; 
 `.[value]push-2/3@sum-up`
 The default value is `u-` which gives `.u-1/2` &nbsp; `.u-push-2/3@sm-up`
* `$grid-gutter-width` set the width of the guttering.
* `$gutter-lg-width` width of large gutters.
* `$gutter-sm-width` width of small gutters.
* `$grid-font-size` Due to using inline-blocks on the `.grid__items we have to
 set the font-size on the `.grid` block to zero to remove unwanted whitespace,
 which would otherwise cause the grid to fail.  This font-size value will be
 set on each individual item and should equal the base font size of your project.
* `$grid-breakpoints` is a nested Sass list that contains all the grid's 
breakpoints that will be used on width, push and pull classes.  
You can remove unused breakpoints, add in your own, customize the breakpoint's
namespace.

###Feature toggle
A list of feature switches, that are all set to true by default.  Set any that
you are not using to false to keep out as much bloat as possible from the
resulting CSS.
* `$use-grid` skeleton of the grid system.
* `$use-grid--equal-height` equal height grid items.
* `$use-grid--centered` vertically center grid items.
* `$use-grid--bottom` vertically align grid-items to the bottom.
* `$use-grid--gutter-lg` larger gutter.
* `$use-grid--gutter-sm` smaller gutter.
* `$use-grid--no-gutter` remove gutter.
* `$use-grid--matrix` vertical gutter matching horizontal gutter.
* `$use-grid--reverse` reverse horizontal ordering of grid items.

You can also toggle specific width, push and pull classes.  Responsive classes
are controlled by the `$grid-breakpoints` list in the `VARS` section and are
automatically added to activated width, push and pull classes.

##Useage
rbrtsmith grids is easy to use and customize.
Using [BEMIT](http://csswizardry.com/2015/08/bemit-taking-the-bem-naming-convention-a-step-further/#responsive-suffixes) 
based class names the markup becomes extremely descriptive and concise.  
Those not familiar with BEMIT here's a short introduction&helipp;
###BEMIT
Based on [BEM](http://csswizardry.com/2013/01/mindbemding-getting-your-head-round-bem-syntax/) 
which stands for **B**lock **E**lement **M**odifier.  BEMIT extends
on BEM to add in additional prefixing and responsive suffixes to better describe
the intentions of the components.
* `.grid` is a **B**lock
* `.grid--equal-height` is a **M**odifier signified by `--`
* `.grid__item` is an **E**lement signified by `__` which is a descendant
of a block.

**BEMIT prefixes**
I use the [ITCSS](https://twitter.com/itcss_io) system in my projects so I have 
added **Object** and **Utility** prefixes to this grid that better describe 
where they live within ITCSS.  
* `o-grid` is an object class
* `o-grid__item` is also an object class.
* `u-1/2` &nbsp; `u-push-2/3` are both utility classes.

**BEMIT responsive suffixes**
* `u-1/2@sm-up` has the responsive suffix that suggests that this class will
be applied to screens larger than the `sm` breakpoint and up. the `sm-up`
namespace can be modified via `$grid-breakpoints` in the `VARS` section.

Further examples of responsive suffixes:
* `u-push-2/3@lg-up`
* `u-pull-5/6@xs-up`

##Acknowledgments
This grid system is Heavily influenced by the great work of
[@csswizardry](https://twitter.com/csswizardry])'s own grid system 
[csswizardry-grids](https://github.com/csswizardry/csswizardry-grids).  

If you haven't already had the privilege of reading Harry's blog then I really 
urge you to dive right in.  It's quite literally a goldmine of useful 
information and techniques.
[http://csswizardry.com](http://csswizardry.com)




