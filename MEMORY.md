# A specification for the memory module

Vardi shall have 64 KiB of byte-addressable memory. There shall be no segmentation of the memory space. 

## Constraints

* Maximum 64KiB of memory

* Minimum 64KiB of memory

* Flat memory model

* 16-bit addresses

## API

* store (:uint16 addr, :uint8 val) :boolean

* fetch (:uint16 addr, :uint8 val) :uint8

* clear (:uint16 addr)

* exist (:uint16 addr) :boolean
