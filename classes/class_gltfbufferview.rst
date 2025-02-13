:github_url: hide

.. DO NOT EDIT THIS FILE!!!
.. Generated automatically from Godot engine sources.
.. Generator: https://github.com/godotengine/godot/tree/master/doc/tools/make_rst.py.
.. XML source: https://github.com/godotengine/godot/tree/master/modules/gltf/doc_classes/GLTFBufferView.xml.

.. _class_GLTFBufferView:

GLTFBufferView
==============

**Inherits:** :ref:`Resource<class_Resource>` **<** :ref:`RefCounted<class_RefCounted>` **<** :ref:`Object<class_Object>`

Represents a GLTF buffer view.

.. rst-class:: classref-introduction-group

Description
-----------

GLTFBufferView is a data structure representing GLTF a ``bufferView`` that would be found in the ``"bufferViews"`` array. A buffer is a blob of binary data. A buffer view is a slice of a buffer that can be used to identify and extract data from the buffer.

Most custom uses of buffers only need to use the :ref:`buffer<class_GLTFBufferView_property_buffer>`, :ref:`byte_length<class_GLTFBufferView_property_byte_length>`, and :ref:`byte_offset<class_GLTFBufferView_property_byte_offset>`. The :ref:`byte_stride<class_GLTFBufferView_property_byte_stride>` and :ref:`indices<class_GLTFBufferView_property_indices>` properties are for more advanced use cases such as interleaved mesh data encoded for the GPU.

.. rst-class:: classref-introduction-group

Tutorials
---------

- `Buffers, BufferViews, and Accessors in Khronos glTF specification <https://github.com/KhronosGroup/glTF-Tutorials/blob/master/gltfTutorial/gltfTutorial_005_BuffersBufferViewsAccessors.md>`__

- :doc:`Runtime file loading and saving <../tutorials/io/runtime_file_loading_and_saving>`

.. rst-class:: classref-reftable-group

Properties
----------

.. table::
   :widths: auto

   +-------------------------+---------------------------------------------------------------+-----------+
   | :ref:`int<class_int>`   | :ref:`buffer<class_GLTFBufferView_property_buffer>`           | ``-1``    |
   +-------------------------+---------------------------------------------------------------+-----------+
   | :ref:`int<class_int>`   | :ref:`byte_length<class_GLTFBufferView_property_byte_length>` | ``0``     |
   +-------------------------+---------------------------------------------------------------+-----------+
   | :ref:`int<class_int>`   | :ref:`byte_offset<class_GLTFBufferView_property_byte_offset>` | ``0``     |
   +-------------------------+---------------------------------------------------------------+-----------+
   | :ref:`int<class_int>`   | :ref:`byte_stride<class_GLTFBufferView_property_byte_stride>` | ``-1``    |
   +-------------------------+---------------------------------------------------------------+-----------+
   | :ref:`bool<class_bool>` | :ref:`indices<class_GLTFBufferView_property_indices>`         | ``false`` |
   +-------------------------+---------------------------------------------------------------+-----------+

.. rst-class:: classref-reftable-group

Methods
-------

.. table::
   :widths: auto

   +-----------------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------+
   | :ref:`PackedByteArray<class_PackedByteArray>` | :ref:`load_buffer_view_data<class_GLTFBufferView_method_load_buffer_view_data>` **(** :ref:`GLTFState<class_GLTFState>` state **)** |const| |
   +-----------------------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------+

.. rst-class:: classref-section-separator

----

.. rst-class:: classref-descriptions-group

Property Descriptions
---------------------

.. _class_GLTFBufferView_property_buffer:

.. rst-class:: classref-property

:ref:`int<class_int>` **buffer** = ``-1``

.. rst-class:: classref-property-setget

- void **set_buffer** **(** :ref:`int<class_int>` value **)**
- :ref:`int<class_int>` **get_buffer** **(** **)**

The index of the buffer this buffer view is referencing. If ``-1``, this buffer view is not referencing any buffer.

.. rst-class:: classref-item-separator

----

.. _class_GLTFBufferView_property_byte_length:

.. rst-class:: classref-property

:ref:`int<class_int>` **byte_length** = ``0``

.. rst-class:: classref-property-setget

- void **set_byte_length** **(** :ref:`int<class_int>` value **)**
- :ref:`int<class_int>` **get_byte_length** **(** **)**

The length, in bytes, of this buffer view. If ``0``, this buffer view is empty.

.. rst-class:: classref-item-separator

----

.. _class_GLTFBufferView_property_byte_offset:

.. rst-class:: classref-property

:ref:`int<class_int>` **byte_offset** = ``0``

.. rst-class:: classref-property-setget

- void **set_byte_offset** **(** :ref:`int<class_int>` value **)**
- :ref:`int<class_int>` **get_byte_offset** **(** **)**

The offset, in bytes, from the start of the buffer to the start of this buffer view.

.. rst-class:: classref-item-separator

----

.. _class_GLTFBufferView_property_byte_stride:

.. rst-class:: classref-property

:ref:`int<class_int>` **byte_stride** = ``-1``

.. rst-class:: classref-property-setget

- void **set_byte_stride** **(** :ref:`int<class_int>` value **)**
- :ref:`int<class_int>` **get_byte_stride** **(** **)**

The stride, in bytes, between interleaved data. If ``-1``, this buffer view is not interleaved.

.. rst-class:: classref-item-separator

----

.. _class_GLTFBufferView_property_indices:

.. rst-class:: classref-property

:ref:`bool<class_bool>` **indices** = ``false``

.. rst-class:: classref-property-setget

- void **set_indices** **(** :ref:`bool<class_bool>` value **)**
- :ref:`bool<class_bool>` **get_indices** **(** **)**

True if the GLTFBufferView's OpenGL GPU buffer type is an ``ELEMENT_ARRAY_BUFFER`` used for vertex indices (integer constant ``34963``). False if the buffer type is ``ARRAY_BUFFER`` used for vertex attributes (integer constant ``34962``) or when any other value. See `Buffers, BufferViews, and Accessors <https://github.com/KhronosGroup/glTF-Tutorials/blob/master/gltfTutorial/gltfTutorial_005_BuffersBufferViewsAccessors.md>`__ for possible values. This property is set but never used, setting this property will do nothing.

.. rst-class:: classref-section-separator

----

.. rst-class:: classref-descriptions-group

Method Descriptions
-------------------

.. _class_GLTFBufferView_method_load_buffer_view_data:

.. rst-class:: classref-method

:ref:`PackedByteArray<class_PackedByteArray>` **load_buffer_view_data** **(** :ref:`GLTFState<class_GLTFState>` state **)** |const|

Loads the buffer view data from the buffer referenced by this buffer view in the given :ref:`GLTFState<class_GLTFState>`. Interleaved data with a byte stride is not yet supported by this method. The data is returned as a :ref:`PackedByteArray<class_PackedByteArray>`.

.. |virtual| replace:: :abbr:`virtual (This method should typically be overridden by the user to have any effect.)`
.. |const| replace:: :abbr:`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
.. |vararg| replace:: :abbr:`vararg (This method accepts any number of arguments after the ones described here.)`
.. |constructor| replace:: :abbr:`constructor (This method is used to construct a type.)`
.. |static| replace:: :abbr:`static (This method doesn't need an instance to be called, so it can be called directly using the class name.)`
.. |operator| replace:: :abbr:`operator (This method describes a valid operator to use with this type as left-hand operand.)`
.. |bitfield| replace:: :abbr:`BitField (This value is an integer composed as a bitmask of the following flags.)`
