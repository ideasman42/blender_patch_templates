
Blender Patch Templates
#######################

This repository is meant to host patches which apply to the Blender ``git.blender.org``, which are good examples of
how to add functionality.

Motivation
==========

Blender is a complex application, some changes may end up needing to touch C, C++, Python and build systems
(CMake). This increases the barrier of entry to anyone who is interested to become involved.

Tutorials _can_ work, often however you end up copying and pasting from them; when they become outdated,
it is not always clear if the changes are made incorrectly or if the tutorial itself is wrong.


Proposal
========

While we can't expect to make this process _easy_, we can at least provide some examples to help developers.

This repository plans to host multiple patches, each of which can be applied on its own and which makes some addition
to Blender that can serve as a basis for further work.


Goals
-----

- Help new developers understand Blender's code-base.
- Patches should be well commented, to help in understanding the purpose of changes.
- Patches should be easily manipulated and customized once applied.
- Patches should be up to date and apply to the latest revision of Blender's git repository.


Pitfalls
--------

There are some things which we would like to avoid:


Cargo Cult Programming
^^^^^^^^^^^^^^^^^^^^^^

*Developers applying changes without understanding what they do.*

The purpose of these patches is teaching you how to quickly identify what changes are needed and how to extend them
for your own use - rather than blindly copying changes and expecting them to work,
just because you followed the template.
Admittedly, early on, many developers will do their fair share of copy-paste from existing code,
but we would encourage developers to take the time to understand all necesssary changes.


New Features (because we can!)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Generally the bottleneck with the development is _not_ that we can't add new features fast enough.

New features are of course interesting, but if you can quickly edit one of these patches to add a new feature,
this is a hint that probably any of Blender's existing developers could have added this too,
and you may need to expand upon it some more, or that the feature may need to be part of some larger project if you want to have it accepted back into Blender.

Having said that, making small changes is a great way to learn.


Prerequisites
=============

To make use of these patches, you should have Blender building and a development environment setup.

See:

- http://wiki.blender.org/index.php/Dev:Doc/Building_Blender
- http://wiki.blender.org/index.php/Dev:Doc/New_Developer_Env
- https://wiki.blender.org/index.php/Dev:Doc/New_Developer_Advice


Usage
=====

Each patch is comprised of 2 files, a read-me and a diff, which can be applied to Blenders source using, eg.

.. code-block::

    git apply modifier_deform.diff

If any of the patches fail to apply to the latest Blender version, please report an issue.
However, you can always check out the version of Blender which the patch was made against.


Patches
=======

Currently this is more of a TODO list.

*Done*

- ``modifier_deform.diff`` simple deformation modifier (moves vertices).
- ``object_add_mesh.diff`` creates a new primitive type (Wedge).

*TODO*

- ``modifier_generate.diff`` simple modifier which generates new geometry.
- ``sequencer_type.diff`` define a new sequence strip type.
- ``texture_type.diff`` define a new texture type.
- ``cycles_shader_node.diff`` define a new Cycles shader type.
- ``compositor_node.diff`` define new compositor node.
- ``editmesh_tool.diff`` edit-mode mesh tool.
- ``editcurve_tool.diff`` edit-mode curve tool.
- ``ui_button_type.diff`` define a new button type.


Contributing Back
=================

If the patch is finished and you believe it to be useful to include in Blender releases, you can submit the patch here.

Blender's developer site: http://developer.blender.org
Under the **BF Blender** heading, **Submit Code**

