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

* fetch (:uint16 addr) :uint8
    This function shall fetch an 8-bit unsigned integer at the given memory address. It shall return the 8-bit unsigned integer if it exists. Uninitialized memory is undefined.

* clear (:uint16 addr) :void
    This function shall write the zero byte `0x0` at the given memory address. It shall not return a value.

## Memory-based IO devices

IO devices MAY be implemented as memory-mapped addresses. If they are then the following addresses SHALL be reserved and MUST NOT be writable.

* 0x101F SHALL enumerate the available input devices
* 0x10F0 SHALL enumerate the available output devices

Additionally, the following address MUST be writable.

* 0x10EE SHALL be a general-purpose signaling location for device-specific errors

An IO device SHALL consist of the following byte-fields
* addr[0] IOP_DONE_FLAG
* addr[1] READABLE_BYTE | WRITABLE_BYTE
* addr[2] READABLE_BYTE | WRITABLE_BYTE
* addr[3] IOP_ERROR_FLAG

The behaviour of the IOP_DONE_FLAG is simple
* `0x1` after a WRITE operation has finished
* `0x0` after a READ operation has finished. 

IOP_ERROR_FLAG SHALL be `0x1` if an IO error has occurred. 
Additional data MAY be present in the general-purpose signaling address `0x10EE`.




