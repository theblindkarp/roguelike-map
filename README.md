# roguelike-map

#### By: Nicholas P. Norman
#### April 2023

# Main Goal

The goal of this project is to create an algorithm that can make command-line "map" that generates randomly with rooms and paths.

# Use Case

This can be used by a command-line game developer to generate maps.

# Input

An amount of columns and rows.

# Output

A command-line ouput and an linked-list.

#### Expected Output

Where 'X' represents a node with an associated object.

----x- <br>
-xx-x- <br>
--xxx- <br>
--x--- <br>

## Classes

```mermaid
classDiagram
    class Node {
        +setNext(Node next)
        +getNext()
        +setPrevious(Node next)
        +getPrevious()
    }

    <<Interface>> Node

    class RowNode {
        string symbol
        RowNode next
        RowNode previous
        +RowNode()
        +setSymbol()
        +getSymbol()
    }

    class ColNode {
        RowNode head
        RowNode tail
        ColNode next
        ColNode previous
        +ColNode()
    }

    class LLMap {
        ColNode head
        ColNode tail
        +LLMap()
    }

    class LinkedList {
        +setHead(Node head)
        +getHead()
        +setTail(Node tail)
        +getTail()
        +append()
        +add(int index)
        +pop(int index) Node
        +size()
    }
    <<Interace>> LinkedList

    class Item {
        String symbol
        int layer
        String name
        int[2] coord
    }

    RowNode <-- ColNode
```
