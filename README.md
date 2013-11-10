jekyll-liquid-lipsum-plugin
==========================

[Jekyll](http://Jekyllrb.com/) plugin that defines a useful Liquid Tag for rendering random paragraphs of text (Lorem ipsum's style) inside a post.

Installation
============

Just copy the `liquid_lipsum.rb` file to your `_plugins` folder.

Requirements
============

None. :)

Configuration
=============

None. :)

Usage
============

It's usage is simple. For example, you insert this line in one of your posts:

    {% lipsum %}

And you'll get something like this:

> Aenean id lacinia neque nec bibendum odio risus a arcu imperdiet metus id velit augue id magna iaculis quis, pretium quam iaculis quis, sit amet nibh ullamcorper nec, pretium quam nonummy ac, erat libero tristique tellus, turpis at pulvinar vulputate, sed nisl molestie nec bibendum odio risus erat libero tristique tellus, a arcu imperdiet pretium quam turpis at pulvinar vulputate, sit amet nibh rutrum non, pretium quam augue id magna ullamcorper nec, porttitor ut, porttitor ut, nec bibendum odio risus sit amet nibh sit amet ante.

As you can see, a full paragraph of random text will substitute the original liquid tag.

Each paragraph will have a beginning, a middle part and an ending. The _size_ of the paragraph corresponds to the number of middle parts. A number of 3 will have 3 middle parts.

The following paragraph has a size of 1: Nam quis nulla ullamcorper nec, sit amet ante. The begining is "Nam quis nulla", the middle part is "ullamcorper nec," and the ending is "sit amet ante".

The beginings, middle parts and endings are taken randomly from 3 different pools of text.

The tag allows up to three numbers as parameters:

* The **first number** represents the number of paragraphs to be generated,
* The **second number** is the minimum size of the paragraph (number of middle parts). 
* The **third number** is the maximum size of the paragraph (number of middle parts).

Combining this, you can have the following situations:

Usage                                     | Result
:-----------------------------------------|:-----------------------------------------------
{%raw%}``{% lipsum %}``{%endraw%}         | 1 paragraph. Random length between 10 and 30
{%raw%}``{% lipsum n %}``{%endraw%}       | **_n_** paragraphs. Random length between 10 and 30
{%raw%}``{% lipsum n l %}``{%endraw%}     | **_n_** paragraphs. Exactly a length of **_l_**
{%raw%}``{% lipsum n l1 l2 %}``{%endraw%} | **_n_** paragraphs. Random length between **_l1_** and **_l2_**
{: .centered title="Use cases of the tag" }

You can improve or modify the behaviour of this liquid tag by simply editing its source code. There you can change the sentence parts to your wishes by simply editing the three arrays of strings from which the generator takes the text parts.

More information
================

Take a look at my [http://www.flx.cat/jekyll/2013/11/09/liquid-lipsum-jekyll-plugin.html](http://www.flx.cat/jekyll/2013/11/09/liquid-lipsum-jekyll-plugin.html) blog entry!
