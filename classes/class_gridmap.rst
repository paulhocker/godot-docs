.. Generated automatically by doc/tools/makerst.py in Godot's source tree.
.. DO NOT EDIT THIS FILE, but the GridMap.xml source instead.
.. The source is found in doc/classes or modules/<name>/doc_classes.

.. _class_GridMap:

GridMap
=======

**Inherits:** :ref:`Spatial<class_spatial>` **<** :ref:`Node<class_node>` **<** :ref:`Object<class_object>`

**Category:** Core

Brief Description
-----------------

Node for 3D tile-based maps.

Member Functions
----------------

+--------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| void                           | :ref:`clear<class_GridMap_clear>` **(** **)**                                                                                                                                                            |
+--------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| void                           | :ref:`clear_baked_meshes<class_GridMap_clear_baked_meshes>` **(** **)**                                                                                                                                  |
+--------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`RID<class_rid>`          | :ref:`get_bake_mesh_instance<class_GridMap_get_bake_mesh_instance>` **(** :ref:`int<class_int>` idx **)**                                                                                                |
+--------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`Array<class_array>`      | :ref:`get_bake_meshes<class_GridMap_get_bake_meshes>` **(** **)**                                                                                                                                        |
+--------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`int<class_int>`          | :ref:`get_cell_item<class_GridMap_get_cell_item>` **(** :ref:`int<class_int>` x, :ref:`int<class_int>` y, :ref:`int<class_int>` z **)** const                                                            |
+--------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`int<class_int>`          | :ref:`get_cell_item_orientation<class_GridMap_get_cell_item_orientation>` **(** :ref:`int<class_int>` x, :ref:`int<class_int>` y, :ref:`int<class_int>` z **)** const                                    |
+--------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`bool<class_bool>`        | :ref:`get_collision_layer_bit<class_GridMap_get_collision_layer_bit>` **(** :ref:`int<class_int>` bit **)** const                                                                                        |
+--------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`bool<class_bool>`        | :ref:`get_collision_mask_bit<class_GridMap_get_collision_mask_bit>` **(** :ref:`int<class_int>` bit **)** const                                                                                          |
+--------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`Array<class_array>`      | :ref:`get_meshes<class_GridMap_get_meshes>` **(** **)**                                                                                                                                                  |
+--------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`Array<class_array>`      | :ref:`get_used_cells<class_GridMap_get_used_cells>` **(** **)** const                                                                                                                                    |
+--------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| void                           | :ref:`make_baked_meshes<class_GridMap_make_baked_meshes>` **(** :ref:`bool<class_bool>` gen_lightmap_uv=false, :ref:`float<class_float>` lightmap_uv_texel_size=0.1 **)**                                |
+--------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`Vector3<class_vector3>`  | :ref:`map_to_world<class_GridMap_map_to_world>` **(** :ref:`int<class_int>` x, :ref:`int<class_int>` y, :ref:`int<class_int>` z **)** const                                                              |
+--------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| void                           | :ref:`resource_changed<class_GridMap_resource_changed>` **(** :ref:`Resource<class_resource>` resource **)**                                                                                             |
+--------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| void                           | :ref:`set_cell_item<class_GridMap_set_cell_item>` **(** :ref:`int<class_int>` x, :ref:`int<class_int>` y, :ref:`int<class_int>` z, :ref:`int<class_int>` item, :ref:`int<class_int>` orientation=0 **)** |
+--------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| void                           | :ref:`set_clip<class_GridMap_set_clip>` **(** :ref:`bool<class_bool>` enabled, :ref:`bool<class_bool>` clipabove=true, :ref:`int<class_int>` floor=0, :ref:`Axis<enum_vector3_axis>` axis=0 **)**        |
+--------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| void                           | :ref:`set_collision_layer_bit<class_GridMap_set_collision_layer_bit>` **(** :ref:`int<class_int>` bit, :ref:`bool<class_bool>` value **)**                                                               |
+--------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| void                           | :ref:`set_collision_mask_bit<class_GridMap_set_collision_mask_bit>` **(** :ref:`int<class_int>` bit, :ref:`bool<class_bool>` value **)**                                                                 |
+--------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`Vector3<class_vector3>`  | :ref:`world_to_map<class_GridMap_world_to_map>` **(** :ref:`Vector3<class_vector3>` pos **)** const                                                                                                      |
+--------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

Member Variables
----------------

  .. _class_GridMap_cell_center_x:

- :ref:`bool<class_bool>` **cell_center_x** - If ``true`` grid items are centered on the X axis.

  .. _class_GridMap_cell_center_y:

- :ref:`bool<class_bool>` **cell_center_y** - If ``true`` grid items are centered on the Y axis.

  .. _class_GridMap_cell_center_z:

- :ref:`bool<class_bool>` **cell_center_z** - If ``true`` grid items are centered on the Z axis.

  .. _class_GridMap_cell_octant_size:

- :ref:`int<class_int>` **cell_octant_size** - The size of each octant measured in number of cells. This applies to all three axis.

  .. _class_GridMap_cell_scale:

- :ref:`float<class_float>` **cell_scale**

  .. _class_GridMap_cell_size:

- :ref:`Vector3<class_vector3>` **cell_size** - The dimensions of the grid's cells.

  .. _class_GridMap_collision_layer:

- :ref:`int<class_int>` **collision_layer**

  .. _class_GridMap_collision_mask:

- :ref:`int<class_int>` **collision_mask**

  .. _class_GridMap_theme:

- :ref:`MeshLibrary<class_meshlibrary>` **theme** - The assigned :ref:`MeshLibrary<class_meshlibrary>`.


Numeric Constants
-----------------

- **INVALID_CELL_ITEM** = **-1** --- Invalid cell item that can be used in :ref:`set_cell_item<class_GridMap_set_cell_item>` to clear cells (or represent an empty cell in :ref:`get_cell_item<class_GridMap_get_cell_item>`).

Description
-----------

GridMap lets you place meshes on a grid interactively. It works both from the editor and can help you create in-game level editors.

GridMaps use a :ref:`MeshLibrary<class_meshlibrary>` which contain a list of tiles: meshes with materials plus optional collisions and extra elements.

A GridMap contains a collection of cells. Each grid cell refers to a :ref:`MeshLibrary<class_meshlibrary>` item. All cells in the map have the same dimensions.

A GridMap is split into a sparse collection of octants for efficient rendering and physics processing. Every octant has the same dimensions and can contain several cells.

Member Function Description
---------------------------

.. _class_GridMap_clear:

- void **clear** **(** **)**

Clear all cells.

.. _class_GridMap_clear_baked_meshes:

- void **clear_baked_meshes** **(** **)**

.. _class_GridMap_get_bake_mesh_instance:

- :ref:`RID<class_rid>` **get_bake_mesh_instance** **(** :ref:`int<class_int>` idx **)**

.. _class_GridMap_get_bake_meshes:

- :ref:`Array<class_array>` **get_bake_meshes** **(** **)**

.. _class_GridMap_get_cell_item:

- :ref:`int<class_int>` **get_cell_item** **(** :ref:`int<class_int>` x, :ref:`int<class_int>` y, :ref:`int<class_int>` z **)** const

The :ref:`MeshLibrary<class_meshlibrary>` item index located at the grid-based X, Y and Z coordinates. If the cell is empty, INVALID_CELL_ITEM will be returned.

.. _class_GridMap_get_cell_item_orientation:

- :ref:`int<class_int>` **get_cell_item_orientation** **(** :ref:`int<class_int>` x, :ref:`int<class_int>` y, :ref:`int<class_int>` z **)** const

The orientation of the cell at the grid-based X, Y and Z coordinates. -1 is retuned if the cell is empty.

.. _class_GridMap_get_collision_layer_bit:

- :ref:`bool<class_bool>` **get_collision_layer_bit** **(** :ref:`int<class_int>` bit **)** const

.. _class_GridMap_get_collision_mask_bit:

- :ref:`bool<class_bool>` **get_collision_mask_bit** **(** :ref:`int<class_int>` bit **)** const

.. _class_GridMap_get_meshes:

- :ref:`Array<class_array>` **get_meshes** **(** **)**

Array of :ref:`Transform<class_transform>` and :ref:`Mesh<class_mesh>` references corresponding to the non empty cells in the grid. The transforms are specified in world space.

.. _class_GridMap_get_used_cells:

- :ref:`Array<class_array>` **get_used_cells** **(** **)** const

Array of :ref:`Vector3<class_vector3>` with the non empty cell coordinates in the grid map.

.. _class_GridMap_make_baked_meshes:

- void **make_baked_meshes** **(** :ref:`bool<class_bool>` gen_lightmap_uv=false, :ref:`float<class_float>` lightmap_uv_texel_size=0.1 **)**

.. _class_GridMap_map_to_world:

- :ref:`Vector3<class_vector3>` **map_to_world** **(** :ref:`int<class_int>` x, :ref:`int<class_int>` y, :ref:`int<class_int>` z **)** const

.. _class_GridMap_resource_changed:

- void **resource_changed** **(** :ref:`Resource<class_resource>` resource **)**

.. _class_GridMap_set_cell_item:

- void **set_cell_item** **(** :ref:`int<class_int>` x, :ref:`int<class_int>` y, :ref:`int<class_int>` z, :ref:`int<class_int>` item, :ref:`int<class_int>` orientation=0 **)**

Set the mesh index for the cell referenced by its grid-based X, Y and Z coordinates.

A negative item index will clear the cell.

Optionally, the item's orientation can be passed.

.. _class_GridMap_set_clip:

- void **set_clip** **(** :ref:`bool<class_bool>` enabled, :ref:`bool<class_bool>` clipabove=true, :ref:`int<class_int>` floor=0, :ref:`Axis<enum_vector3_axis>` axis=0 **)**

.. _class_GridMap_set_collision_layer_bit:

- void **set_collision_layer_bit** **(** :ref:`int<class_int>` bit, :ref:`bool<class_bool>` value **)**

.. _class_GridMap_set_collision_mask_bit:

- void **set_collision_mask_bit** **(** :ref:`int<class_int>` bit, :ref:`bool<class_bool>` value **)**

.. _class_GridMap_world_to_map:

- :ref:`Vector3<class_vector3>` **world_to_map** **(** :ref:`Vector3<class_vector3>` pos **)** const


