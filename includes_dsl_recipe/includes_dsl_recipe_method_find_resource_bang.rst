.. The contents of this file may be included in multiple topics (using the includes directive).
.. The contents of this file should be modified in a way that preserves its ability to appear in multiple topics.


Use the ``find_resource!`` method to find a resource in the resource collection. If the resource is not found, an exception is returned.

The syntax for the ``find_resource!`` method is as follows:

.. code-block:: ruby

   find_resource!(:resource_type, 'resource_name')

where:

* ``:resource_type`` is the resource type, such as ``:file ``(for the |resource file| resource), ``:template`` (for the |resource template| resource), and so on. Any resource available to |chef| may be declared.
* ``resource_name`` the property that is the default name of the resource, typically the string that appears in the ``resource 'name' do`` block of a resource (but not always); see the Syntax section for the resource to be declared to verify the default name property.

For example:

.. code-block:: ruby

   find_resource!(:template, '/x/y.erb')
