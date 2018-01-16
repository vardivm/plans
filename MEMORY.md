# A specification for the memory module

Vardi shall have 64 KiB of byte-addressable memory. There shall be no segmentation of the memory space. 

## Constraints

* Maximum 64KiB of memory

* Minimum 64KiB of memory

* Flat memory model

* 16-bit addresses

## API

* store (:uint16 addr, :uint8 val) :boolean
    This function shall store an 8-bit unsigned integer at the given memory address. It shall return true if the address exists and a write was successful.

* fetch (:uint16 addr, :uint8 val) :uint8
    This function shall fetch an 8-bit unsigned integer at the given memory address. It shall return the 8-bit unsigned integer if it exists. Uninitialized memory is undefined.

* clear (:uint16 addr) :void
    This function shall write the zero byte `0x0` at the given memory address. It shall not return a value.


