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

To access an element in a linked list, we start from the first node and then work across the entire structure node-by-node until the desired node is reached. When doing this, it is important to be careful not to use the initial variable storing the head, as Linked Lists must be maintained in memory, and updating a variable storing the head of a Linked List leads to the pre-update value being destroyed. This is different from a python `List` type or an Array in other languages, where indexing is a reference-only operation. 

Linked Lists are good at sequential or ordered tasks, but bad at performing random access.  
### Variants of Linked Lists
#### Doubly Linked Lists
A Doubly Linked list is exactly like a traditional Linked List (also called a 'Singly Linked List'), but with each node containing a `next` and a `prev` pointer, which point to the next node and the previous node, respectively.

```drawio
<mxfile host="embed.diagrams.net">
  <diagram id="8bwthM2Xe25gGJqiUHln" name="Page-1">
    <mxGraphModel dx="1616" dy="921" grid="1" gridSize="10" guides="1" tooltips="1" connect="1"
        arrows="1" fold="1" page="1" pageScale="1" pageWidth="827" pageHeight="1169" math="0"
        shadow="0">
      <root>
        <mxCell id="0" />
        <mxCell id="1" parent="0" />
        <mxCell id="-hsYzijuVU9oEN3qOrYB-4" parent="1" style="whiteSpace=wrap;html=1;aspect=fixed;"
            value="&#39;A&#39;" vertex="1">
          <mxGeometry height="40" width="40" x="200" y="320" as="geometry" />
        </mxCell>
        <mxCell id="-hsYzijuVU9oEN3qOrYB-5" parent="1" style="whiteSpace=wrap;html=1;aspect=fixed;"
            value="&#39;l&#39;" vertex="1">
          <mxGeometry height="40" width="40" x="320" y="320" as="geometry" />
        </mxCell>
        <mxCell id="-hsYzijuVU9oEN3qOrYB-7" parent="1" style="whiteSpace=wrap;html=1;aspect=fixed;"
            value="&#39;g&#39;" vertex="1">
          <mxGeometry height="40" width="40" x="440" y="320" as="geometry" />
        </mxCell>
        <mxCell id="-hsYzijuVU9oEN3qOrYB-9" parent="1" style="whiteSpace=wrap;html=1;aspect=fixed;"
            value="&#39;o&#39;" vertex="1">
          <mxGeometry height="40" width="40" x="560" y="320" as="geometry" />
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
            <mxPoint x="449" y="252" as="targetPoint" />
          </mxGeometry>
        </mxCell>
        <mxCell id="-hsYzijuVU9oEN3qOrYB-13" parent="1" style="whiteSpace=wrap;html=1;aspect=fixed;"
            value="" vertex="1">
          <mxGeometry height="40" width="40" x="320" y="280" as="geometry" />
        </mxCell>
        <mxCell id="-hsYzijuVU9oEN3qOrYB-14" edge="1" parent="1"
            style="endArrow=classic;html=1;rounded=0;entryX=0;entryY=0.5;entryDx=0;entryDy=0;"
            target="-hsYzijuVU9oEN3qOrYB-7" value="">
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
            target="-hsYzijuVU9oEN3qOrYB-9" value="">
          <mxGeometry height="50" relative="1" width="50" as="geometry">
            <mxPoint x="460" y="300" as="sourcePoint" />
            <mxPoint x="520" y="300" as="targetPoint" />
          </mxGeometry>
        </mxCell>
        <mxCell id="44XN9UBHtgokEOFtZYKK-1" parent="1" style="rounded=0;whiteSpace=wrap;html=1;"
            value="A Doubly Linked List representing the list [ &#39;A&#39;, &#39;l&#39;, &#39;g&#39;, &#39;o&#39; ]"
            vertex="1">
          <mxGeometry height="40" width="440" x="160" y="230" as="geometry" />
        </mxCell>
        <mxCell id="BQ31ehKBwLWymlz-Axsp-1" parent="1" style="whiteSpace=wrap;html=1;aspect=fixed;"
            value="" vertex="1">
          <mxGeometry height="40" width="40" x="200" y="360" as="geometry" />
        </mxCell>
        <mxCell id="BQ31ehKBwLWymlz-Axsp-2" parent="1" style="whiteSpace=wrap;html=1;aspect=fixed;"
            value="" vertex="1">
          <mxGeometry height="40" width="40" x="320" y="360" as="geometry" />
        </mxCell>
        <mxCell id="BQ31ehKBwLWymlz-Axsp-3" parent="1" style="whiteSpace=wrap;html=1;aspect=fixed;"
            value="" vertex="1">
          <mxGeometry height="40" width="40" x="440" y="360" as="geometry" />
        </mxCell>
        <mxCell id="BQ31ehKBwLWymlz-Axsp-4" parent="1" style="whiteSpace=wrap;html=1;aspect=fixed;"
            value="" vertex="1">
          <mxGeometry height="40" width="40" x="560" y="360" as="geometry" />
        </mxCell>
        <mxCell id="BQ31ehKBwLWymlz-Axsp-7" edge="1" parent="1"
            style="endArrow=none;html=1;rounded=0;entryX=0;entryY=0.5;entryDx=0;entryDy=0;startArrow=classic;startFill=1;endFill=0;"
            value="">
          <mxGeometry height="50" relative="1" width="50" as="geometry">
            <mxPoint x="240" y="340" as="sourcePoint" />
            <mxPoint x="340" y="380" as="targetPoint" />
          </mxGeometry>
        </mxCell>
        <mxCell id="BQ31ehKBwLWymlz-Axsp-8" edge="1" parent="1"
            style="endArrow=none;html=1;rounded=0;entryX=0;entryY=0.5;entryDx=0;entryDy=0;startArrow=classic;startFill=1;endFill=0;"
            value="">
          <mxGeometry height="50" relative="1" width="50" as="geometry">
            <mxPoint x="360" y="340" as="sourcePoint" />
            <mxPoint x="460" y="380" as="targetPoint" />
          </mxGeometry>
        </mxCell>
        <mxCell id="BQ31ehKBwLWymlz-Axsp-9" edge="1" parent="1"
            style="endArrow=none;html=1;rounded=0;entryX=0;entryY=0.5;entryDx=0;entryDy=0;startArrow=classic;startFill=1;endFill=0;"
            value="">
          <mxGeometry height="50" relative="1" width="50" as="geometry">
            <mxPoint x="480" y="340" as="sourcePoint" />
            <mxPoint x="580" y="380" as="targetPoint" />
          </mxGeometry>
        </mxCell>
        <mxCell id="BQ31ehKBwLWymlz-Axsp-10" parent="1"
            style="text;html=1;whiteSpace=wrap;strokeColor=none;fillColor=none;align=center;verticalAlign=middle;rounded=0;"
            value="next" vertex="1">
          <mxGeometry height="30" width="60" x="150" y="285" as="geometry" />
        </mxCell>
        <mxCell id="BQ31ehKBwLWymlz-Axsp-11" parent="1"
            style="text;html=1;whiteSpace=wrap;strokeColor=none;fillColor=none;align=center;verticalAlign=middle;rounded=0;"
            value="prev" vertex="1">
          <mxGeometry height="30" width="60" x="150" y="365" as="geometry" />
        </mxCell>
      </root>
    </mxGraphModel>
  </diagram>
</mxfile>
```
The double-link system means that traversal across the list is freely available, and therefore indexing operations and random access are both much faster that they would be in the case of traditional linked lists. 
#### Linked Lists with Attributes
Occasionally, you might come across Linked Lists which also store other attributes or properties of the linked list, for a number of different reasons:
- **A pointer to the 'tail'** - this would make it much easier to append to the end of the linked list, (debatably) count the number of elements, reverse the list, or remove things from the end. Any applications which are largely sequential but require rapid addition to the end of the list. 
- **A length or size** - This would save you the need to iterate (or recurse!) across the linked list in order to get the length/size. It would also save the need to blindly check for the end of the list

There are other attributes that you may need to store in order to best suit your use-case. Generally, this is done by having a standard `ListNode` implementation as the core data structure, with a wrapper type/class that stores the head of the list and everything else you may need:

```java
public class ListNode {
    public int elem;
    public ListNode nxt;
	...
}

public class LinkedList {
    private ListNode head;
    // attributes here
    private ListNode tail;
    private int len;
	...
	
    public LinkedList() {
        this.head = new ListNode();
        this.tail = this.head;
        this.len = 0;
    }
}
```

Remember that we cannot just blindly use all of these all the time. Storing these attributes adds bulk to the initial list, and it also makes all of our operations more complex. It is also important to keep in mind that this new wrapper Linked List would need to be set up in such as way that it ensure the attributed do not go out of sync.
#### Cyclic Linked Lists
Any time you need to perform cyclical or repeating operations/functions, the tail of a linked list can be linked to the head. 
To do this, we would also need a wrapper, and this time we do need to store the *first element*, the *last element* and the *length*.
## Trees
Trees are a generalisation of Linked lists. They are similarly composed of nodes, but instead of each node having a link to a node in a linear series, it has any number of links to any number of nodes. 

```drawio
<mxfile host="embed.diagrams.net">
  <diagram id="60YzqIwmpjZrrPGEojwZ" name="Page-1">
    <mxGraphModel dx="1374" dy="783" grid="1" gridSize="10" guides="1" tooltips="1" connect="1"
        arrows="1" fold="1" page="1" pageScale="1" pageWidth="827" pageHeight="1169" math="0"
        shadow="0">
      <root>
        <mxCell id="0" />
        <mxCell id="1" parent="0" />
        <mxCell id="J1dqFXJVVMeItZVsS6UM-1" parent="1"
            style="ellipse;whiteSpace=wrap;html=1;shapeInside=1;aspect=fixed;" value="child lvl2"
            vertex="1">
          <mxGeometry height="80" width="80" x="220" y="400" as="geometry" />
        </mxCell>
        <mxCell id="J1dqFXJVVMeItZVsS6UM-2" parent="1"
            style="ellipse;whiteSpace=wrap;html=1;shapeInside=1;aspect=fixed;" value="child lvl2"
            vertex="1">
          <mxGeometry height="80" width="80" x="510" y="230" as="geometry" />
        </mxCell>
        <mxCell id="J1dqFXJVVMeItZVsS6UM-9" edge="1" parent="1" source="J1dqFXJVVMeItZVsS6UM-3"
            style="edgeStyle=orthogonalEdgeStyle;rounded=0;orthogonalLoop=1;jettySize=auto;html=1;"
            target="J1dqFXJVVMeItZVsS6UM-6" value="">
          <mxGeometry relative="1" as="geometry" />
        </mxCell>
        <mxCell id="J1dqFXJVVMeItZVsS6UM-10" edge="1" parent="1" source="J1dqFXJVVMeItZVsS6UM-3"
            style="rounded=0;orthogonalLoop=1;jettySize=auto;html=1;exitX=0;exitY=1;exitDx=0;exitDy=0;entryX=1;entryY=0;entryDx=0;entryDy=0;"
            target="J1dqFXJVVMeItZVsS6UM-1">
          <mxGeometry relative="1" as="geometry" />
        </mxCell>
        <mxCell id="J1dqFXJVVMeItZVsS6UM-3" parent="1"
            style="ellipse;whiteSpace=wrap;html=1;shapeInside=1;aspect=fixed;" value="child lvl1"
            vertex="1">
          <mxGeometry height="80" width="80" x="374" y="240" as="geometry" />
        </mxCell>
        <mxCell id="J1dqFXJVVMeItZVsS6UM-4" parent="1"
            style="ellipse;whiteSpace=wrap;html=1;shapeInside=1;aspect=fixed;" value="child lvl2"
            vertex="1">
          <mxGeometry height="80" width="80" x="640" y="140" as="geometry" />
        </mxCell>
        <mxCell id="J1dqFXJVVMeItZVsS6UM-15" edge="1" parent="1" source="J1dqFXJVVMeItZVsS6UM-5"
            style="edgeStyle=orthogonalEdgeStyle;rounded=0;orthogonalLoop=1;jettySize=auto;html=1;"
            target="J1dqFXJVVMeItZVsS6UM-2" value="">
          <mxGeometry relative="1" as="geometry" />
        </mxCell>
        <mxCell id="J1dqFXJVVMeItZVsS6UM-16" edge="1" parent="1" source="J1dqFXJVVMeItZVsS6UM-5"
            style="rounded=0;orthogonalLoop=1;jettySize=auto;html=1;"
            target="J1dqFXJVVMeItZVsS6UM-4" value="">
          <mxGeometry relative="1" as="geometry" />
        </mxCell>
        <mxCell id="J1dqFXJVVMeItZVsS6UM-5" parent="1"
            style="ellipse;whiteSpace=wrap;html=1;shapeInside=1;aspect=fixed;" value="child lvl1"
            vertex="1">
          <mxGeometry height="80" width="80" x="510" y="90" as="geometry" />
        </mxCell>
        <mxCell id="J1dqFXJVVMeItZVsS6UM-6" parent="1"
            style="ellipse;whiteSpace=wrap;html=1;shapeInside=1;aspect=fixed;" value="child lvl2"
            vertex="1">
          <mxGeometry height="80" width="80" x="374" y="400" as="geometry" />
        </mxCell>
        <mxCell id="J1dqFXJVVMeItZVsS6UM-7" parent="1"
            style="ellipse;whiteSpace=wrap;html=1;shapeInside=1;aspect=fixed;" value="child lvl1"
            vertex="1">
          <mxGeometry height="80" width="80" x="220" y="170" as="geometry" />
        </mxCell>
        <mxCell id="J1dqFXJVVMeItZVsS6UM-11" edge="1" parent="1" source="J1dqFXJVVMeItZVsS6UM-8"
            style="edgeStyle=orthogonalEdgeStyle;rounded=0;orthogonalLoop=1;jettySize=auto;html=1;"
            target="J1dqFXJVVMeItZVsS6UM-3" value="">
          <mxGeometry relative="1" as="geometry" />
        </mxCell>
        <mxCell id="J1dqFXJVVMeItZVsS6UM-12" edge="1" parent="1" source="J1dqFXJVVMeItZVsS6UM-8"
            style="rounded=0;orthogonalLoop=1;jettySize=auto;html=1;exitX=0;exitY=0.5;exitDx=0;exitDy=0;entryX=1;entryY=0;entryDx=0;entryDy=0;"
            target="J1dqFXJVVMeItZVsS6UM-7">
          <mxGeometry relative="1" as="geometry" />
        </mxCell>
        <mxCell id="J1dqFXJVVMeItZVsS6UM-13" edge="1" parent="1" source="J1dqFXJVVMeItZVsS6UM-8"
            style="rounded=0;orthogonalLoop=1;jettySize=auto;html=1;exitX=1;exitY=0.5;exitDx=0;exitDy=0;"
            target="J1dqFXJVVMeItZVsS6UM-5">
          <mxGeometry relative="1" as="geometry" />
        </mxCell>
        <mxCell id="J1dqFXJVVMeItZVsS6UM-8" parent="1"
            style="ellipse;whiteSpace=wrap;html=1;shapeInside=1;aspect=fixed;" value="root"
            vertex="1">
          <mxGeometry height="80" width="80" x="374" y="30" as="geometry" />
        </mxCell>
      </root>
    </mxGraphModel>
  </diagram>
</mxfile>
```

For ease, we refer to the origin of a link as the *parent* node. Each node to which the parent has a link is known as a *child* of that node. All nodes in a tree must have *one and only one* parent **except for one single node**. This parent-less node is known as the *root* node. This means that trees are not allowed to have 'cycles' (more on this is the Graphs section).

Another way of thinking about this is that the 'links' in trees will always have an explicit origin and destination. No two sets of links originating at the same node will terminate at the same node.

For some node *n* in a tree, the number of nodes that must be visited before reaching it (starting at the root) is known as the *height* of that node. The height of the node that is **furthest from the root** is called the height of the tree. Each new link leads to an increase in the height of the tree. A full path starting at the root and going to a node which has no children is called a branch of the tree. 

There are also some special constraints that can be applied to trees, which are helpful in algorithms:
- **Binary Tree**: A tree where each node has a maximum of two children
- **Balanced Tree**: A tree where there are never two branches whose height difference is more than 1.  
- **Binary Search Tree**: A binary tree where, for each parent node, the left-child-value is less than or equal to the right-child-value
## Graphs
Graphs are a further generalisation of Trees. They are also comprised of nodes, each of which are linked to other nodes.  There is no distinction between parent and child nodes in trees, and 'links' are actually called 'edges'. Unlike Trees, the multiple groups of edges leading to a single node can also have the same origin. In other words, unlike Trees, edges in graphs can 'go in circles'. This is called a cycle. 
### Properties of Graphs
#### Directed/Undirected Graphs
Edges in Graphs connect two node. In **Directed** Graphs, these edges have an origin and a destination, which also define a direction of traversal. In **Undirected** Graphs, edges don't have a direction. 

This has a lot of interesting implications when using graphs to model problems or algorithms. For instance, a directed graphs works for systems of nodes where you are trying to calculate the cost of traversal. A extremely common use case is for pathfinding algorithms - like a primitive version of the algorithm used by Google Maps to find optimal routes.
```drawio
<mxfile host="embed.diagrams.net">
  <diagram id="AuPiNinhdYixl8GdPoeO" name="Page-1">
    <mxGraphModel dx="851" dy="509" grid="1" gridSize="10" guides="1" tooltips="1" connect="1"
        arrows="1" fold="1" page="1" pageScale="1" pageWidth="827" pageHeight="1169" math="0"
        shadow="0">
      <root>
        <mxCell id="0" />
        <mxCell id="1" parent="0" />
        <mxCell id="B0-La0ow3tp3BnGaxLZG-9" edge="1" parent="1" source="B0-La0ow3tp3BnGaxLZG-2"
            style="edgeStyle=orthogonalEdgeStyle;rounded=0;orthogonalLoop=1;jettySize=auto;html=1;"
            target="B0-La0ow3tp3BnGaxLZG-6" value="">
          <mxGeometry relative="1" as="geometry" />
        </mxCell>
        <mxCell id="B0-La0ow3tp3BnGaxLZG-2" parent="1"
            style="ellipse;whiteSpace=wrap;html=1;shapeInside=1;aspect=fixed;" value="" vertex="1">
          <mxGeometry height="40" width="40" x="280" y="200" as="geometry" />
        </mxCell>
        <mxCell id="B0-La0ow3tp3BnGaxLZG-3" parent="1"
            style="ellipse;whiteSpace=wrap;html=1;shapeInside=1;aspect=fixed;" value="Main Library"
            vertex="1">
          <mxGeometry height="60" width="60" x="620" y="190" as="geometry" />
        </mxCell>
        <mxCell id="B0-La0ow3tp3BnGaxLZG-13" edge="1" parent="1" source="B0-La0ow3tp3BnGaxLZG-4"
            style="edgeStyle=orthogonalEdgeStyle;rounded=0;orthogonalLoop=1;jettySize=auto;html=1;"
            target="B0-La0ow3tp3BnGaxLZG-2" value="">
          <mxGeometry relative="1" as="geometry" />
        </mxCell>
        <mxCell id="B0-La0ow3tp3BnGaxLZG-16" edge="1" parent="1" source="B0-La0ow3tp3BnGaxLZG-4"
            style="edgeStyle=orthogonalEdgeStyle;rounded=0;orthogonalLoop=1;jettySize=auto;html=1;exitX=0.5;exitY=0;exitDx=0;exitDy=0;entryX=0.5;entryY=0;entryDx=0;entryDy=0;curved=1;fillColor=#60a917;strokeColor=#2D7600;"
            target="B0-La0ow3tp3BnGaxLZG-3">
          <mxGeometry relative="1" as="geometry">
            <Array as="points">
              <mxPoint x="190" y="90" />
              <mxPoint x="650" y="90" />
            </Array>
          </mxGeometry>
        </mxCell>
        <mxCell id="B0-La0ow3tp3BnGaxLZG-4" parent="1"
            style="ellipse;whiteSpace=wrap;html=1;shapeInside=1;aspect=fixed;" value="Jack Cole Lab"
            vertex="1">
          <mxGeometry height="60" width="60" x="160" y="190" as="geometry" />
        </mxCell>
        <mxCell id="B0-La0ow3tp3BnGaxLZG-11" edge="1" parent="1" source="B0-La0ow3tp3BnGaxLZG-5"
            style="edgeStyle=orthogonalEdgeStyle;rounded=0;orthogonalLoop=1;jettySize=auto;html=1;"
            target="B0-La0ow3tp3BnGaxLZG-7" value="">
          <mxGeometry relative="1" as="geometry" />
        </mxCell>
        <mxCell id="B0-La0ow3tp3BnGaxLZG-5" parent="1"
            style="ellipse;whiteSpace=wrap;html=1;shapeInside=1;aspect=fixed;" value="" vertex="1">
          <mxGeometry height="40" width="40" x="440" y="200" as="geometry" />
        </mxCell>
        <mxCell id="B0-La0ow3tp3BnGaxLZG-10" edge="1" parent="1" source="B0-La0ow3tp3BnGaxLZG-6"
            style="edgeStyle=orthogonalEdgeStyle;rounded=0;orthogonalLoop=1;jettySize=auto;html=1;"
            target="B0-La0ow3tp3BnGaxLZG-5" value="">
          <mxGeometry relative="1" as="geometry" />
        </mxCell>
        <mxCell id="B0-La0ow3tp3BnGaxLZG-6" parent="1"
            style="ellipse;whiteSpace=wrap;html=1;shapeInside=1;aspect=fixed;" value="" vertex="1">
          <mxGeometry height="40" width="40" x="360" y="200" as="geometry" />
        </mxCell>
        <mxCell id="B0-La0ow3tp3BnGaxLZG-14" edge="1" parent="1" source="B0-La0ow3tp3BnGaxLZG-7"
            style="edgeStyle=orthogonalEdgeStyle;rounded=0;orthogonalLoop=1;jettySize=auto;html=1;"
            target="B0-La0ow3tp3BnGaxLZG-3" value="">
          <mxGeometry relative="1" as="geometry" />
        </mxCell>
        <mxCell id="B0-La0ow3tp3BnGaxLZG-7" parent="1"
            style="ellipse;whiteSpace=wrap;html=1;shapeInside=1;aspect=fixed;" value="" vertex="1">
          <mxGeometry height="40" width="40" x="520" y="200" as="geometry" />
        </mxCell>
        <mxCell id="mqkPWpPDb7nUBedtAPmc-1" parent="1"
            style="text;html=1;whiteSpace=wrap;strokeColor=none;fillColor=none;align=center;verticalAlign=middle;rounded=0;"
            value="not to scale (and don&#39;t use this as a map, you will end up in the sea instead of the Main Library"
            vertex="1">
          <mxGeometry height="30" width="390" x="350" y="270" as="geometry" />
        </mxCell>
      </root>
    </mxGraphModel>
  </diagram>
</mxfile>
```
Of course, this particular graph makes it very clear that there is more information needed, since the selected route (in green) is obviously longer. 
#### Weighted Edges
In cases where not all edges of a graph can be treated as equivalent, edges can be assigned a *'weight'*, which is a number associated with it that can be used as a linear quantifier for some quality associated with the graph.

Consider the Google Maps example from above. Trying to find an optimal route could be improved by taking into account the time needed to walk down a lane that joins two junctions (represented by nodes). 

For example, if a lane is 1 kilometre long, we could give it a weight of 1. For a lane that is 5km long, we could take a weight of 5 (and so forth). Without weights, it seems like five edges is always a worse path than one edge. With weights, we can make the distinction that five edges, each of weight 1 is better than one edge of weight 10.

```drawio
<mxfile host="embed.diagrams.net">
  <diagram id="AuPiNinhdYixl8GdPoeO" name="Page-1">
    <mxGraphModel dx="993" dy="593" grid="1" gridSize="10" guides="1" tooltips="1" connect="1"
        arrows="1" fold="1" page="1" pageScale="1" pageWidth="827" pageHeight="1169" math="0"
        shadow="0">
      <root>
        <mxCell id="0" />
        <mxCell id="1" parent="0" />
        <mxCell id="B0-La0ow3tp3BnGaxLZG-9" edge="1" parent="1" source="B0-La0ow3tp3BnGaxLZG-2"
            style="edgeStyle=orthogonalEdgeStyle;rounded=0;orthogonalLoop=1;jettySize=auto;html=1;fillColor=#60a917;strokeColor=#2D7600;"
            target="B0-La0ow3tp3BnGaxLZG-6" value="">
          <mxGeometry relative="1" as="geometry" />
        </mxCell>
        <mxCell id="bt4MJI-toOqRqbceL6wK-3" connectable="0" parent="B0-La0ow3tp3BnGaxLZG-9"
            style="edgeLabel;html=1;align=center;verticalAlign=middle;resizable=0;points=[];"
            value="1" vertex="1">
          <mxGeometry relative="1" x="-0.1829" y="-2" as="geometry">
            <mxPoint y="-3" as="offset" />
          </mxGeometry>
        </mxCell>
        <mxCell id="B0-La0ow3tp3BnGaxLZG-2" parent="1"
            style="ellipse;whiteSpace=wrap;html=1;shapeInside=1;aspect=fixed;fillColor=#60a917;fontColor=#ffffff;strokeColor=#2D7600;"
            value="" vertex="1">
          <mxGeometry height="40" width="40" x="280" y="200" as="geometry" />
        </mxCell>
        <mxCell id="B0-La0ow3tp3BnGaxLZG-3" parent="1"
            style="ellipse;whiteSpace=wrap;html=1;shapeInside=1;aspect=fixed;" value="Main Library"
            vertex="1">
          <mxGeometry height="60" width="60" x="620" y="190" as="geometry" />
        </mxCell>
        <mxCell id="B0-La0ow3tp3BnGaxLZG-13" edge="1" parent="1" source="B0-La0ow3tp3BnGaxLZG-4"
            style="edgeStyle=orthogonalEdgeStyle;rounded=0;orthogonalLoop=1;jettySize=auto;html=1;fillColor=#60a917;strokeColor=#2D7600;"
            target="B0-La0ow3tp3BnGaxLZG-2" value="">
          <mxGeometry relative="1" as="geometry" />
        </mxCell>
        <mxCell id="bt4MJI-toOqRqbceL6wK-2" connectable="0" parent="B0-La0ow3tp3BnGaxLZG-13"
            style="edgeLabel;html=1;align=center;verticalAlign=middle;resizable=0;points=[];"
            value="1" vertex="1">
          <mxGeometry relative="1" x="-0.1886" y="1" as="geometry">
            <mxPoint as="offset" />
          </mxGeometry>
        </mxCell>
        <mxCell id="B0-La0ow3tp3BnGaxLZG-16" edge="1" parent="1" source="B0-La0ow3tp3BnGaxLZG-4"
            style="edgeStyle=orthogonalEdgeStyle;rounded=0;orthogonalLoop=1;jettySize=auto;html=1;exitX=0.5;exitY=0;exitDx=0;exitDy=0;entryX=0.5;entryY=0;entryDx=0;entryDy=0;curved=1;"
            target="B0-La0ow3tp3BnGaxLZG-3">
          <mxGeometry relative="1" as="geometry">
            <Array as="points">
              <mxPoint x="190" y="90" />
              <mxPoint x="650" y="90" />
            </Array>
          </mxGeometry>
        </mxCell>
        <mxCell id="bt4MJI-toOqRqbceL6wK-1" connectable="0" parent="B0-La0ow3tp3BnGaxLZG-16"
            style="edgeLabel;html=1;align=center;verticalAlign=middle;resizable=0;points=[];"
            value="w = 10" vertex="1">
          <mxGeometry relative="1" x="-0.0414" as="geometry">
            <mxPoint x="14" as="offset" />
          </mxGeometry>
        </mxCell>
        <mxCell id="B0-La0ow3tp3BnGaxLZG-4" parent="1"
            style="ellipse;whiteSpace=wrap;html=1;shapeInside=1;aspect=fixed;" value="Jack Cole Lab"
            vertex="1">
          <mxGeometry height="60" width="60" x="160" y="190" as="geometry" />
        </mxCell>
        <mxCell id="B0-La0ow3tp3BnGaxLZG-11" edge="1" parent="1" source="B0-La0ow3tp3BnGaxLZG-5"
            style="edgeStyle=orthogonalEdgeStyle;rounded=0;orthogonalLoop=1;jettySize=auto;html=1;fillColor=#60a917;strokeColor=#2D7600;"
            target="B0-La0ow3tp3BnGaxLZG-7" value="">
          <mxGeometry relative="1" as="geometry" />
        </mxCell>
        <mxCell id="bt4MJI-toOqRqbceL6wK-5" connectable="0" parent="B0-La0ow3tp3BnGaxLZG-11"
            style="edgeLabel;html=1;align=center;verticalAlign=middle;resizable=0;points=[];"
            value="1" vertex="1">
          <mxGeometry relative="1" x="-0.1829" y="-2" as="geometry">
            <mxPoint x="1" y="-3" as="offset" />
          </mxGeometry>
        </mxCell>
        <mxCell id="B0-La0ow3tp3BnGaxLZG-5" parent="1"
            style="ellipse;whiteSpace=wrap;html=1;shapeInside=1;aspect=fixed;fillColor=#60a917;fontColor=#ffffff;strokeColor=#2D7600;"
            value="" vertex="1">
          <mxGeometry height="40" width="40" x="440" y="200" as="geometry" />
        </mxCell>
        <mxCell id="B0-La0ow3tp3BnGaxLZG-10" edge="1" parent="1" source="B0-La0ow3tp3BnGaxLZG-6"
            style="edgeStyle=orthogonalEdgeStyle;rounded=0;orthogonalLoop=1;jettySize=auto;html=1;fillColor=#60a917;strokeColor=#2D7600;"
            target="B0-La0ow3tp3BnGaxLZG-5" value="">
          <mxGeometry relative="1" as="geometry" />
        </mxCell>
        <mxCell id="bt4MJI-toOqRqbceL6wK-4" connectable="0" parent="B0-La0ow3tp3BnGaxLZG-10"
            style="edgeLabel;html=1;align=center;verticalAlign=middle;resizable=0;points=[];"
            value="1" vertex="1">
          <mxGeometry relative="1" x="0.0171" as="geometry">
            <mxPoint x="-3" y="-1" as="offset" />
          </mxGeometry>
        </mxCell>
        <mxCell id="B0-La0ow3tp3BnGaxLZG-6" parent="1"
            style="ellipse;whiteSpace=wrap;html=1;shapeInside=1;aspect=fixed;fillColor=#60a917;fontColor=#ffffff;strokeColor=#2D7600;"
            value="" vertex="1">
          <mxGeometry height="40" width="40" x="360" y="200" as="geometry" />
        </mxCell>
        <mxCell id="B0-La0ow3tp3BnGaxLZG-14" edge="1" parent="1" source="B0-La0ow3tp3BnGaxLZG-7"
            style="edgeStyle=orthogonalEdgeStyle;rounded=0;orthogonalLoop=1;jettySize=auto;html=1;fillColor=#60a917;strokeColor=#2D7600;"
            target="B0-La0ow3tp3BnGaxLZG-3" value="">
          <mxGeometry relative="1" as="geometry" />
        </mxCell>
        <mxCell id="bt4MJI-toOqRqbceL6wK-6" connectable="0" parent="B0-La0ow3tp3BnGaxLZG-14"
            style="edgeLabel;html=1;align=center;verticalAlign=middle;resizable=0;points=[];"
            value="1" vertex="1">
          <mxGeometry relative="1" x="-0.1553" y="1" as="geometry">
            <mxPoint as="offset" />
          </mxGeometry>
        </mxCell>
        <mxCell id="B0-La0ow3tp3BnGaxLZG-7" parent="1"
            style="ellipse;whiteSpace=wrap;html=1;shapeInside=1;aspect=fixed;fillColor=#60a917;fontColor=#ffffff;strokeColor=#2D7600;"
            value="" vertex="1">
          <mxGeometry height="40" width="40" x="520" y="200" as="geometry" />
        </mxCell>
      </root>
    </mxGraphModel>
  </diagram>
</mxfile>
```
