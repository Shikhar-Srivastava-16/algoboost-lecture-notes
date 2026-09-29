## Linked Lists

**Linked Lists** are the simplest of the recursive data structures that we will cover. It is a simple collection without any real structure. The most basic unit of a Linked List is a *Node*, which contains two data points - a **value** and a **pointer**. 

```drawio
<mxfile host="embed.diagrams.net">
  <diagram id="8bwthM2Xe25gGJqiUHln" name="Page-1">
    <mxGraphModel dx="1056" dy="618" grid="1" gridSize="10" guides="1" tooltips="1" connect="1"
        arrows="1" fold="1" page="1" pageScale="1" pageWidth="827" pageHeight="1169" math="0"
        shadow="0">
      <root>
        <mxCell id="0" />
        <mxCell id="1" parent="0" />
        <mxCell id="-hsYzijuVU9oEN3qOrYB-4" parent="1" style="whiteSpace=wrap;html=1;aspect=fixed;"
            value="&#39;A&#39;" vertex="1">
          <mxGeometry height="40" width="40" x="160" y="280" as="geometry" />
        </mxCell>
        <mxCell id="-hsYzijuVU9oEN3qOrYB-5" parent="1" style="whiteSpace=wrap;html=1;aspect=fixed;"
            value="&#39;l&#39;" vertex="1">
          <mxGeometry height="40" width="40" x="280" y="280" as="geometry" />
        </mxCell>
        <mxCell id="-hsYzijuVU9oEN3qOrYB-7" parent="1" style="whiteSpace=wrap;html=1;aspect=fixed;"
            value="&#39;g&#39;" vertex="1">
          <mxGeometry height="40" width="40" x="400" y="280" as="geometry" />
        </mxCell>
        <mxCell id="-hsYzijuVU9oEN3qOrYB-9" parent="1" style="whiteSpace=wrap;html=1;aspect=fixed;"
            value="&#39;o&#39;" vertex="1">
          <mxGeometry height="40" width="40" x="520" y="280" as="geometry" />
        </mxCell>
        <mxCell id="-hsYzijuVU9oEN3qOrYB-10" parent="1" style="whiteSpace=wrap;html=1;aspect=fixed;"
            value="" vertex="1">
          <mxGeometry height="40" width="40" x="560" y="280" as="geometry" />
        </mxCell>
        <mxCell id="-hsYzijuVU9oEN3qOrYB-11" parent="1" style="whiteSpace=wrap;html=1;aspect=fixed;"
            value="" vertex="1">
          <mxGeometry height="40" width="40" x="200" y="280" as="geometry" />
        </mxCell>
        <mxCell id="-hsYzijuVU9oEN3qOrYB-12" edge="1" parent="1"
            style="endArrow=classic;html=1;rounded=0;entryX=0;entryY=0.5;entryDx=0;entryDy=0;"
            target="-hsYzijuVU9oEN3qOrYB-5" value="">
          <mxGeometry height="50" relative="1" width="50" as="geometry">
            <mxPoint x="220" y="300" as="sourcePoint" />
            <mxPoint x="409" y="212" as="targetPoint" />
          </mxGeometry>
        </mxCell>
        <mxCell id="-hsYzijuVU9oEN3qOrYB-13" parent="1" style="whiteSpace=wrap;html=1;aspect=fixed;"
            value="" vertex="1">
          <mxGeometry height="40" width="40" x="320" y="280" as="geometry" />
        </mxCell>
        <mxCell id="-hsYzijuVU9oEN3qOrYB-14" edge="1" parent="1"
            style="endArrow=classic;html=1;rounded=0;entryX=0;entryY=0.5;entryDx=0;entryDy=0;"
            value="">
          <mxGeometry height="50" relative="1" width="50" as="geometry">
            <mxPoint x="340" y="300" as="sourcePoint" />
            <mxPoint x="400" y="300" as="targetPoint" />
          </mxGeometry>
        </mxCell>
        <mxCell id="-hsYzijuVU9oEN3qOrYB-15" parent="1" style="whiteSpace=wrap;html=1;aspect=fixed;"
            value="" vertex="1">
          <mxGeometry height="40" width="40" x="440" y="280" as="geometry" />
        </mxCell>
        <mxCell id="-hsYzijuVU9oEN3qOrYB-16" edge="1" parent="1"
            style="endArrow=classic;html=1;rounded=0;entryX=0;entryY=0.5;entryDx=0;entryDy=0;"
            value="">
          <mxGeometry height="50" relative="1" width="50" as="geometry">
            <mxPoint x="460" y="300" as="sourcePoint" />
            <mxPoint x="520" y="300" as="targetPoint" />
          </mxGeometry>
        </mxCell>
        <mxCell id="44XN9UBHtgokEOFtZYKK-1" parent="1" style="rounded=0;whiteSpace=wrap;html=1;"
            value="A Linked List representing the list [ &#39;A&#39;, &#39;l&#39;, &#39;g&#39;, &#39;o&#39; ]"
            vertex="1">
          <mxGeometry height="40" width="440" x="160" y="230" as="geometry" />
        </mxCell>
      </root>
    </mxGraphModel>
  </diagram>
</mxfile>
```

The value contains the element of the list which is stored in that node. The pointer goes to the address of the following node, which represents the following element of the list. The first node of a linked list is often called the **head node** or simply the **head** of the list. The last node  is likewise called the **tail** or **tail node**.

(Diagram)

To access an element in a linked list, we start from the first node and then work across the entire structure node-by-node until the desired node is reached. When doing this, it is important to be careful not to use the initial variable storing the head, as Linked Lists must be maintained in memory, and updating a variable storing the head of a Linked List leads to the pre-update value being destroyed. This is different from a python `List` type or an Array in other languages, where indexing is a reference-only operation. 

Linked Lists are good at sequential or ordered tasks, but bad at performing random access.  
### Variants of Linked Lists
#### Doubly Linked Lists

A Doubly Linked list is exactly like a traditional Linked List (also called a 'Singly Linked List'), but with each node containing a `next` and a `prev` pointer, which point to the next node and the previous node, respectively. 
#### Tail Linked Lists
#### Cyclic Linked Lists
## Trees

Trees are a generalisation 

## Graphs