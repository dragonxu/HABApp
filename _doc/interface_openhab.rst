.. _ref_openhab:

openHAB
==================================

Interaction with a openHAB
------------------------------
All interaction with the openHAB is done through the ``self.oh`` or ``self.openhab`` object in the rule.

.. image:: /gifs/openhab.gif



Function parameters
------------------------------
.. autoclass:: HABApp.openhab.oh_interface.OpenhabInterface
   :members:

.. autoclass:: HABApp.openhab.oh_interface.OpenhabItemDefinition


Openhab item types
------------------------------

Openhab items are mapped to special classes and provide convenience functions.

Example:

.. execute_code::

    # hide
    import HABApp
    from HABApp.openhab.items import ContactItem, SwitchItem
    HABApp.core.Items.set_item(ContactItem('MyContact', initial_value='OPEN'))
    HABApp.core.Items.set_item(SwitchItem('MySwitch', initial_value='OFF'))
    # hide

    my_contact = ContactItem.get_item('MyContact')
    if my_contact.is_open():
        print('Contact is open!')

    my_switch = SwitchItem.get_item('MySwitch')
    if my_switch.is_on():
        my_switch.off()

.. list-table::
   :widths: auto
   :header-rows: 1

   * - Openhab type
     - HABApp class
   * - ``NumberItem``
     - :class:`~HABApp.openhab.items.NumberItem`
   * - ``Contact``
     - :class:`~HABApp.openhab.items.ContactItem`
   * - ``Switch``
     - :class:`~HABApp.openhab.items.SwitchItem`
   * - ``Dimmer``
     - :class:`~HABApp.openhab.items.DimmerItem`
   * - ``Rollershutter``
     - :class:`~HABApp.openhab.items.RollershutterItem`
   * - ``Color``
     - :class:`~HABApp.openhab.items.ColorItem`
   * - ``String``
     - :class:`~HABApp.openhab.items.StringItem`
   * - ``Location``
     - :class:`~HABApp.openhab.items.LocationItem`
   * - ``Player``
     - :class:`~HABApp.openhab.items.PlayerItem`
   * - ``Image``
     - :class:`~HABApp.openhab.items.ImageItem`
   * - ``Group``
     - :class:`~HABApp.openhab.items.GroupItem`
   * - ``Thing``
     - :class:`~HABApp.openhab.items.Thing`


.. inheritance-diagram:: HABApp.openhab.items.NumberItem
   :parts: 1

.. autoclass:: HABApp.openhab.items.NumberItem
   :members:
   :inherited-members:
   :member-order: groupwise


.. inheritance-diagram:: HABApp.openhab.items.ContactItem
   :parts: 1

.. autoclass:: HABApp.openhab.items.ContactItem
   :members:
   :inherited-members:
   :member-order: groupwise


.. inheritance-diagram:: HABApp.openhab.items.SwitchItem
   :parts: 1

.. autoclass:: HABApp.openhab.items.SwitchItem
   :members:
   :inherited-members:
   :member-order: groupwise


.. inheritance-diagram:: HABApp.openhab.items.DimmerItem
   :parts: 1

.. autoclass:: HABApp.openhab.items.DimmerItem
   :members:
   :inherited-members:
   :member-order: groupwise


.. inheritance-diagram:: HABApp.openhab.items.RollershutterItem
   :parts: 1

.. autoclass:: HABApp.openhab.items.RollershutterItem
   :members:
   :inherited-members:
   :member-order: groupwise


.. inheritance-diagram:: HABApp.openhab.items.ColorItem
   :parts: 1

.. autoclass:: HABApp.openhab.items.ColorItem
   :members:
   :inherited-members:
   :member-order: groupwise


.. inheritance-diagram:: HABApp.openhab.items.StringItem
   :parts: 1

.. autoclass:: HABApp.openhab.items.StringItem
   :members:
   :inherited-members:
   :member-order: groupwise


.. inheritance-diagram:: HABApp.openhab.items.LocationItem
   :parts: 1

.. autoclass:: HABApp.openhab.items.LocationItem
   :members:
   :inherited-members:
   :member-order: groupwise


.. inheritance-diagram:: HABApp.openhab.items.PlayerItem
   :parts: 1

.. autoclass:: HABApp.openhab.items.PlayerItem
   :members:
   :inherited-members:
   :member-order: groupwise


.. inheritance-diagram:: HABApp.openhab.items.GroupItem
   :parts: 1

.. autoclass:: HABApp.openhab.items.GroupItem
   :members:
   :inherited-members:
   :member-order: groupwise


.. inheritance-diagram:: HABApp.openhab.items.Thing
   :parts: 1

.. autoclass:: HABApp.openhab.items.Thing
   :members:
   :inherited-members:
   :member-order: groupwise


.. inheritance-diagram:: HABApp.openhab.items.ImageItem
   :parts: 1

.. autoclass:: HABApp.openhab.items.ImageItem
   :members:
   :inherited-members:
   :member-order: groupwise


Example openHAB rule
---------------------
.. literalinclude:: ../conf/rules/openhab_rule.py
