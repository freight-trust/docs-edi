# Baseline EDI Schema

<span class="sr-only">Toggle navigation</span><span class="icon-bar">
</span><span class="icon-bar"> </span><span class="icon-bar"> </span>

<span class="navbar-brand xs3p-navbar-title">EDI Schema
Documentation</span>

-   [Schema Document Properties](#SchemaProperties)
-   [Global Declarations](#SchemaDeclarations)
-   [Element: **compositeType**](#element_compositeType)
-   [Element: **description**](#element_description)
-   [Element: **elementType**](#element_elementType)
-   [Element: **enumeration**](#element_enumeration)
-   [Element: **implementation**](#element_implementation)
-   [Element: **include**](#element_include)
-   [Element: **interchange**](#element_interchange)
-   [Element: **schema**](#element_schema)
-   [Element: **segmentType**](#element_segmentType)
-   [Element: **syntax**](#element_syntax)
-   [Element: **transaction**](#element_transaction)
-   [Global Definitions](#SchemaDefinitions)
-   [Attribute Group:
    **implementationAttributeGroup**](#attributeGroup_implementationAttributeGroup)
-   [Attribute Group:
    **lengthAttributeGroup**](#attributeGroup_lengthAttributeGroup)
-   [Attribute Group:
    **occursAttributeGroup**](#attributeGroup_occursAttributeGroup)
-   [Attribute Group:
    **referenceAttributeGroup**](#attributeGroup_referenceAttributeGroup)
-   [Attribute Group:
    **versionAttributeGroup**](#attributeGroup_versionAttributeGroup)
-   [Complex Type: **anyElementType**](#type_anyElementType)
-   [Complex Type: **baseType**](#type_baseType)
-   [Complex Type: **compositeImpl**](#type_compositeImpl)
-   [Complex Type: **compositeStandard**](#type_compositeStandard)
-   [Complex Type: **controlType**](#type_controlType)
-   [Complex Type: **elementImpl**](#type_elementImpl)
-   [Complex Type: **elementStandard**](#type_elementStandard)
-   [Complex Type: **groupControlType**](#type_groupControlType)
-   [Complex Type: **loopBase**](#type_loopBase)
-   [Complex Type: **loopImpl**](#type_loopImpl)
-   [Complex Type: **loopStandard**](#type_loopStandard)
-   [Complex Type: **segmentImpl**](#type_segmentImpl)
-   [Complex Type: **segmentStandard**](#type_segmentStandard)
-   [Complex Type:
    **transactionControlType**](#type_transactionControlType)
-   [Simple Type: **discriminatorType**](#type_discriminatorType)
-   [Simple Type: **elementBaseType**](#type_elementBaseType)
-   [Simple Type: **nameType**](#type_nameType)
-   [Simple Type: **positionType**](#type_positionType)
-   [Simple Type: **syntaxType**](#type_syntaxType)
-   [Simple Type: **useType**](#type_useType)
-   [Glossary](#Glossary)


#### Attribute minOccurs

The minimum number of times an undefined element may occur at the
declared location in the EDI structure.

#### Attribute maxOccurs

The maximum number of times an undefined element may occur at the
declared location in the EDI structure.

#### Attribute type

The name of the target type being referenced.

#### Attribute minLength

The minimum length allowed for an element value to be valid.

#### Attribute maxLength

The maximum length allowed for an element value to be valid.

#### Attribute minOccurs

The minimum number of times a type may occur at the declared location in
the EDI structure.

#### Attribute maxOccurs

The maximum number of times a type may occur at the declared location in
the EDI structure.

#### Attribute minVersion

The minimum transaction version this schema version applies to.

#### Attribute maxVersion

The maximum transaction version this schema version applies to.

#### Attribute minOccurs

The minimum number of times a type may occur at the declared location in
the EDI structure.

#### Attribute maxOccurs

The maximum number of times a type may occur at the declared location in
the EDI structure.

#### Element sequence

The ordered elements for a composite element implementation.

#### Element sequence

The ordered elements and components for a segment implementation.

#### Attribute type

The name of the standard segment used at this position in the
implementation. Must be a valid segment name that occurs in the same
standard loop.

#### Attribute code

Code used to identify a segment within a loop. May be useful when
occurrences of a standard segment contain distinct information.

#### Attribute discriminator

The element position in the segment used to identify an occurrence of a
standard segment from other implementation occurrences. The element
identified by the position given in this attribute must also specify an
enumeration of values used only by this implementation and not used by
any other implementations of the standard segment in the same
implementation loop.

#### Attribute minOccurs

The minimum number of times a loop may repeat. A value of 0 (zero)
indicates that the loop is optional. When used in a loop defined within
an implementation, the value may not be less than the value set on the
standard loop referenced by the implementation loop's 'type' attribute.

#### Attribute maxOccurs

The maximum number of times a loop may repeat. When used in a loop
defined within an implementation, the value may not be greater than the
value set on the standard loop referenced by the implementation loop's
'type' attribute.

#### Element sequence

The ordered list of segments and sub-loops contained in this loop.

#### Attribute code

Code used to uniquely identify a loop within the transaction/message.

#### Element sequence

The ordered list of segments and sub-loops contained in this loop.

#### Attribute type

The identifier (code attribute) of the standard loop this loop
implements.

#### Attribute code

Code used to uniquely identify a loop implementation within the
transaction/message implementation.

#### Attribute discriminator

The element position in the loop's first segment used to identify an
implementation of a standard loop from other implementations. The
element identified by the position given in this attribute must also
specify an enumeration of values used only by this implementation and
not used by any other implementations of the standard loop at the same
level of the transaction.

#### Element include

Optional reference to another schema file to include.

#### Element sequence

The ordered list of segments and sub-loops contained at the top-level of
this transaction.

#### Element sequence

The ordered list of segments and sub-loops contained at the top-level of
a transaction implementation.

#### Attribute name

Code used to uniquely identify an element definition to be referenced by
compositeType and segmentType elements within this schema. This value
will be returned by an EDIStreamReader's \`getReferenceCode\` method
when no \`code\` attribute has been specified.

#### Attribute code

Code used to identify an element externally. This value will be returned
by an EDIStreamReader's \`getReferenceCode\` method.

#### Attribute number

\*DEPRECATED\* Use the \`code\` attribute to provide an element
reference number.

#### Attribute base

Identifies the element data type

#### Attribute scale

For numeric base types only, scale is the number of digits to the right
of an implied decimal point. When not specified, the default value of
zero is used (i.e. the data type is integer)

#### Element sequence

The ordered elements and syntax restrictions for a composite element.

#### Element any

May be used to declare that any component element may occur in this
composite type up to the maximum number given by maxOccurs. The value of
minOccurs defines the number of undefined component elements that MUST
occur in the composite.

#### Attribute name

Code used to uniquely identify a composite element definition to be
referenced by segmentType elements within this schema. This value will
be returned by an EDIStreamReader's \`getReferenceCode\` method.

#### Element segmentType

Used to declare a segment

#### Element sequence

The ordered elements, components, and syntax restrictions for a segment.

#### Element element

Defines a reference to a standard element definition.

#### Element any

May be used to declare that any element or composite may occur in this
segment type up to the maximum number given by maxOccurs. The value of
minOccurs defines the number of undefined elements that MUST occur in
the segment at this position. Elements that repeat may occur up to 99
times and are not affected by the value of the maxOccurs attribute.

#### Attribute name

Name of the segment. Also referred to as the segment's tag. This is the
two or three character string used to identify a segment.

Close

<span id="top">EDI Schema Documentation</span>
==============================================

<span id="SchemaProperties">Schema Document Properties</span>
-------------------------------------------------------------

#### <a href="#schema-properties-table-collapse" class="xs3p-panel-title">Properties</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

<table class="table table-striped xs3p-in-panel-table">
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><a href="#term_TargetNS" title="Look up &#39;Target Namespace&#39; in glossary">Target Namespace</a></td>
<td><span class="targetNS">http://freighttrust.io/EDISchema/v4</span></td>
</tr>
<tr class="even">
<td>Element and Attribute Namespaces</td>
<td><ul class="incremental">
<li>Global element and attribute declarations belong to this schema's target namespace.</li>
<li>By default, local element declarations belong to this schema's target namespace.</li>
<li>By default, local attribute declarations have no namespace.</li>
</ul></td>
</tr>
</tbody>
</table>

#### <a href="#schema-doc-panel-collapse" class="xs3p-panel-title">Documentation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

No documentation provided.

#### <a href="#schema-declared-namespaces-collapse" class="xs3p-panel-title">Declared Namespaces</a>

<table class="table table-striped xs3p-in-panel-table">
<thead>
<tr class="header">
<th>Prefix</th>
<th>Namespace</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="ns_">Default namespace</span></td>
<td>http://www.w3.org/2001/XMLSchema</td>
</tr>
<tr class="even">
<td><span id="ns_xml">xml</span></td>
<td>http://www.w3.org/XML/1998/namespace</td>
</tr>
<tr class="odd">
<td><span id="ns_tns">tns</span></td>
<td><span class="targetNS">http://freighttrust.io/EDISchema/v4</span></td>
</tr>
</tbody>
</table>

#### <a href="#schema-schemaComponent-collapse" class="xs3p-panel-title collapsed">Schema Component Representation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

    <schema targetNamespace="http://freighttrust.io/EDISchema/v4" elementFormDefault="qualified">
    ...
    </schema>

[<span class="glyphicon glyphicon-chevron-up">
</span>](#top "Go to top of page")

------------------------------------------------------------------------

<span id="SchemaDeclarations">Global Declarations</span>
--------------------------------------------------------

### Element: <span id="element_compositeType" class="name">compositeType</span>

#### <a href="#element_compositeType-properties-table-collapse" class="xs3p-panel-title">Properties</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

<table class="table table-striped xs3p-in-panel-table">
<tbody>
<tr class="odd">
<td>Name</td>
<td>compositeType</td>
</tr>
<tr class="even">
<td>Type</td>
<td>Locally-defined complex type</td>
</tr>
<tr class="odd">
<td><a href="#term_Nillable" title="Look up &#39;Nillable&#39; in glossary">Nillable</a></td>
<td>no</td>
</tr>
<tr class="even">
<td><a href="#term_Abstract" title="Look up &#39;Abstract&#39; in glossary">Abstract</a></td>
<td>no</td>
</tr>
</tbody>
</table>

#### <a href="#element_compositeType-doc-panel-collapse" class="xs3p-panel-title">Documentation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

No documentation provided.

#### <a href="#element_compositeType-instance-table-collapse" class="xs3p-panel-title">XML Instance Representation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

    <tns:compositeType
     title="string" [0..1]
     name="tns:nameType" [1]×Attribute name
                    Code used to uniquely identify a composite element definition to be referenced by
                    segmentType elements within this schema. This
                    value will be returned by an EDIStreamReader's `getReferenceCode` method.
                   Close  
    >
       <tns:description> ... </tns:description> [0..1]
       <tns:sequence   > [1]   
          Start Choice [1..*]
             <tns:element> tns:elementStandard </tns:element> [1..*]
             <tns:any> tns:anyElementType </tns:any> [1]  
          End Choice
       </tns:sequence>
       <tns:syntax> ... </tns:syntax> [0..*]
    </tns:compositeType>

#### <a href="#element_compositeType-schemaComponent-collapse" class="xs3p-panel-title collapsed">Schema Component Representation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

    <element name="compositeType">
       <complexType>
          <complexContent>
             <extension base="tns:baseType">
                <sequence>
                   <element name="sequence">
                      <complexType>
                         <choice minOccurs="1" maxOccurs="unbounded">
                            <element name="element" type="tns:elementStandard" minOccurs="1" maxOccurs="unbounded"/>
                            <element name="any" type="tns:anyElementType"/>
                         </choice>
                      </complexType>
                   </element>
                   <element ref="tns:syntax" minOccurs="0" maxOccurs="unbounded"/>
                </sequence>
                <attribute name="name" type="tns:nameType" use="required"/>
             </extension>
          </complexContent>
       </complexType>
    </element>

[<span class="glyphicon glyphicon-chevron-up">
</span>](#top "Go to top of page")

------------------------------------------------------------------------

### Element: <span id="element_description" class="name">description</span>

#### <a href="#element_description-properties-table-collapse" class="xs3p-panel-title">Properties</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

<table class="table table-striped xs3p-in-panel-table">
<tbody>
<tr class="odd">
<td>Name</td>
<td>description</td>
</tr>
<tr class="even">
<td>Type</td>
<td><span class="type">string</span></td>
</tr>
<tr class="odd">
<td><a href="#term_Nillable" title="Look up &#39;Nillable&#39; in glossary">Nillable</a></td>
<td>no</td>
</tr>
<tr class="even">
<td><a href="#term_Abstract" title="Look up &#39;Abstract&#39; in glossary">Abstract</a></td>
<td>no</td>
</tr>
</tbody>
</table>

#### <a href="#element_description-doc-panel-collapse" class="xs3p-panel-title">Documentation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

No documentation provided.

#### <a href="#element_description-instance-table-collapse" class="xs3p-panel-title">XML Instance Representation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

    <tns:description> string </tns:description>

#### <a href="#element_description-schemaComponent-collapse" class="xs3p-panel-title collapsed">Schema Component Representation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

    <element name="description" type="string"/>

[<span class="glyphicon glyphicon-chevron-up">
</span>](#top "Go to top of page")

------------------------------------------------------------------------

### Element: <span id="element_elementType" class="name">elementType</span>

#### <a href="#element_elementType-properties-table-collapse" class="xs3p-panel-title">Properties</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

<table class="table table-striped xs3p-in-panel-table">
<tbody>
<tr class="odd">
<td>Name</td>
<td>elementType</td>
</tr>
<tr class="even">
<td>Type</td>
<td>Locally-defined complex type</td>
</tr>
<tr class="odd">
<td><a href="#term_Nillable" title="Look up &#39;Nillable&#39; in glossary">Nillable</a></td>
<td>no</td>
</tr>
<tr class="even">
<td><a href="#term_Abstract" title="Look up &#39;Abstract&#39; in glossary">Abstract</a></td>
<td>no</td>
</tr>
</tbody>
</table>

#### <a href="#element_elementType-doc-panel-collapse" class="xs3p-panel-title">Documentation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

No documentation provided.

#### <a href="#element_elementType-instance-table-collapse" class="xs3p-panel-title">XML Instance Representation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

    <tns:elementType
     title="string" [0..1]
     name="tns:nameType" [1]×Attribute name
                    Code used to uniquely identify an element definition to be referenced by
                    compositeType and segmentType elements within this schema.
                    This value will be returned by an EDIStreamReader's `getReferenceCode` method
                    when no `code` attribute has been specified.
                   Close  
     code="NMTOKEN" [0..1]×Attribute code
                    Code used to identify an element externally. This value will
                    be returned by an EDIStreamReader's `getReferenceCode` method.
                   Close  
     number="nonNegativeInteger (1 <= value <= 9999)" [0..1]×Attribute number*DEPRECATED* Use the `code` attribute to provide an element reference number. Close  
     base="tns:elementBaseType" [0..1]×Attribute base
                    Identifies the element data type
                   Close  
     scale="nonNegativeInteger" [0..1]×Attribute scale
                    For numeric base types only, scale is the number of digits to the right of an implied decimal point. When not specified, the
                    default value of zero is used (i.e. the data type is integer)
                   Close  
     minLength="nonNegativeInteger" [0..1]×Attribute minLength
              The minimum length allowed for an element value to be valid.
             Close  
     maxLength="nonNegativeInteger" [0..1]×Attribute maxLength
              The maximum length allowed for an element value to be valid.
             Close  
    >
       <tns:description> ... </tns:description> [0..1]
       <tns:enumeration> ... </tns:enumeration> [0..1]
       <tns:version
        minVersion="token" [0..1]×Attribute minVersion
              The minimum transaction version this schema version applies to.
             Close  
        maxVersion="token" [0..1]×Attribute maxVersion
              The maximum transaction version this schema version applies to.
             Close  
        minLength="nonNegativeInteger" [0..1]×Attribute minLength
              The minimum length allowed for an element value to be valid.
             Close  
        maxLength="nonNegativeInteger" [0..1]×Attribute maxLength
              The maximum length allowed for an element value to be valid.
             Close  
       > [0..*] 
          <tns:enumeration> ... </tns:enumeration> [0..1]
       </tns:version>
    </tns:elementType>

#### <a href="#element_elementType-schemaComponent-collapse" class="xs3p-panel-title collapsed">Schema Component Representation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

    <element name="elementType">
       <complexType>
          <complexContent>
             <extension base="tns:baseType">
                <sequence>
                   <element ref="tns:enumeration" minOccurs="0"/>
                   <element name="version" minOccurs="0" maxOccurs="unbounded">
                      <complexType>
                         <sequence>
                            <element ref="tns:enumeration" minOccurs="0"/>
                         </sequence>
                         <attributeGroup ref="tns:versionAttributeGroup"/>
                         <attributeGroup ref="tns:lengthAttributeGroup"/>
                      </complexType>
                   </element>
                </sequence>
                <attribute name="name" type="tns:nameType" use="required"/>
                <attribute name="code" type="NMTOKEN" use="optional"/>
                <attribute name="number">
                   <simpleType>
                      <restriction base="nonNegativeInteger">
                         <minInclusive value="1"/>
                         <maxInclusive value="9999"/>
                      </restriction>
                   </simpleType>
                </attribute>
                <attribute name="base" type="tns:elementBaseType" use="optional" default="string"/>
                <attribute name="scale" type="nonNegativeInteger" use="optional" default="0"/>
                <attributeGroup ref="tns:lengthAttributeGroup"/>
             </extension>
          </complexContent>
       </complexType>
    </element>

[<span class="glyphicon glyphicon-chevron-up">
</span>](#top "Go to top of page")

------------------------------------------------------------------------

### Element: <span id="element_enumeration" class="name">enumeration</span>

#### <a href="#element_enumeration-properties-table-collapse" class="xs3p-panel-title">Properties</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

<table class="table table-striped xs3p-in-panel-table">
<tbody>
<tr class="odd">
<td>Name</td>
<td>enumeration</td>
</tr>
<tr class="even">
<td>Type</td>
<td>Locally-defined complex type</td>
</tr>
<tr class="odd">
<td><a href="#term_Nillable" title="Look up &#39;Nillable&#39; in glossary">Nillable</a></td>
<td>no</td>
</tr>
<tr class="even">
<td><a href="#term_Abstract" title="Look up &#39;Abstract&#39; in glossary">Abstract</a></td>
<td>no</td>
</tr>
</tbody>
</table>

#### <a href="#element_enumeration-doc-panel-collapse" class="xs3p-panel-title">Documentation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

No documentation provided.

#### <a href="#element_enumeration-instance-table-collapse" class="xs3p-panel-title">XML Instance Representation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

    <tns:enumeration>
       <tns:value
        title="string" [0..1]
       > [1..*] 
           token
       </tns:value>
    </tns:enumeration>

#### <a href="#element_enumeration-schemaComponent-collapse" class="xs3p-panel-title collapsed">Schema Component Representation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

    <element name="enumeration">
       <complexType>
          <sequence>
             <element name="value" maxOccurs="unbounded">
                <complexType>
                   <simpleContent>
                      <extension base="token">
                         <attribute name="title" type="string"/>
                      </extension>
                   </simpleContent>
                </complexType>
             </element>
          </sequence>
       </complexType>
    </element>

[<span class="glyphicon glyphicon-chevron-up">
</span>](#top "Go to top of page")

------------------------------------------------------------------------

### Element: <span id="element_implementation" class="name">implementation</span>

#### <a href="#element_implementation-properties-table-collapse" class="xs3p-panel-title">Properties</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

<table class="table table-striped xs3p-in-panel-table">
<tbody>
<tr class="odd">
<td>Name</td>
<td>implementation</td>
</tr>
<tr class="even">
<td>Type</td>
<td>Locally-defined complex type</td>
</tr>
<tr class="odd">
<td><a href="#term_Nillable" title="Look up &#39;Nillable&#39; in glossary">Nillable</a></td>
<td>no</td>
</tr>
<tr class="even">
<td><a href="#term_Abstract" title="Look up &#39;Abstract&#39; in glossary">Abstract</a></td>
<td>no</td>
</tr>
</tbody>
</table>

#### <a href="#element_implementation-doc-panel-collapse" class="xs3p-panel-title">Documentation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

No documentation provided.

#### <a href="#element_implementation-instance-table-collapse" class="xs3p-panel-title">XML Instance Representation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

    <tns:implementation
     title="string" [0..1]
    >
       <tns:description> ... </tns:description> [0..1]
       <tns:sequence   > [1]   
          Start Choice [1..*]
             <tns:segment> tns:segmentImpl </tns:segment> [1]
             <tns:loop> tns:loopImpl </tns:loop> [0..1]
          End Choice
       </tns:sequence>
    </tns:implementation>

#### <a href="#element_implementation-schemaComponent-collapse" class="xs3p-panel-title collapsed">Schema Component Representation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

    <element name="implementation">
       <complexType>
          <complexContent>
             <extension base="tns:baseType">
                <sequence>
                   <element name="sequence">
                      <complexType>
                         <choice maxOccurs="unbounded">
                            <element name="segment" type="tns:segmentImpl"/>
                            <element name="loop" type="tns:loopImpl" minOccurs="0"/>
                         </choice>
                      </complexType>
                   </element>
                </sequence>
             </extension>
          </complexContent>
       </complexType>
    </element>

[<span class="glyphicon glyphicon-chevron-up">
</span>](#top "Go to top of page")

------------------------------------------------------------------------

### Element: <span id="element_include" class="name">include</span>

#### <a href="#element_include-properties-table-collapse" class="xs3p-panel-title">Properties</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

<table class="table table-striped xs3p-in-panel-table">
<tbody>
<tr class="odd">
<td>Name</td>
<td>include</td>
</tr>
<tr class="even">
<td>Type</td>
<td>Locally-defined complex type</td>
</tr>
<tr class="odd">
<td><a href="#term_Nillable" title="Look up &#39;Nillable&#39; in glossary">Nillable</a></td>
<td>no</td>
</tr>
<tr class="even">
<td><a href="#term_Abstract" title="Look up &#39;Abstract&#39; in glossary">Abstract</a></td>
<td>no</td>
</tr>
</tbody>
</table>

#### <a href="#element_include-doc-panel-collapse" class="xs3p-panel-title">Documentation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

No documentation provided.

#### <a href="#element_include-instance-table-collapse" class="xs3p-panel-title">XML Instance Representation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

    <tns:include
     schemaLocation="anyURI" [1]
    /> 

#### <a href="#element_include-schemaComponent-collapse" class="xs3p-panel-title collapsed">Schema Component Representation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

    <element name="include">
       <complexType>
          <attribute name="schemaLocation" type="anyURI" use="required"/>
       </complexType>
    </element>

[<span class="glyphicon glyphicon-chevron-up">
</span>](#top "Go to top of page")

------------------------------------------------------------------------

### Element: <span id="element_interchange" class="name">interchange</span>

#### <a href="#element_interchange-properties-table-collapse" class="xs3p-panel-title">Properties</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

<table class="table table-striped xs3p-in-panel-table">
<tbody>
<tr class="odd">
<td>Name</td>
<td>interchange</td>
</tr>
<tr class="even">
<td>Type</td>
<td>Locally-defined complex type</td>
</tr>
<tr class="odd">
<td><a href="#term_Nillable" title="Look up &#39;Nillable&#39; in glossary">Nillable</a></td>
<td>no</td>
</tr>
<tr class="even">
<td><a href="#term_Abstract" title="Look up &#39;Abstract&#39; in glossary">Abstract</a></td>
<td>no</td>
</tr>
</tbody>
</table>

#### <a href="#element_interchange-doc-panel-collapse" class="xs3p-panel-title">Documentation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

No documentation provided.

#### <a href="#element_interchange-instance-table-collapse" class="xs3p-panel-title">XML Instance Representation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

    <tns:interchange
     title="string" [0..1]
     header="NCName" [1]
     trailer="NCName" [1]
    >
       <tns:description> ... </tns:description> [0..1]
       <tns:sequence   > [1] 
          <tns:segment> tns:segmentStandard </tns:segment> [0..*]
          <tns:group> tns:groupControlType </tns:group> [0..1]
          <tns:transaction> tns:transactionControlType </tns:transaction> [0..1]
       </tns:sequence>
       <tns:syntax> ... </tns:syntax> [0..*]
    </tns:interchange>

#### <a href="#element_interchange-schemaComponent-collapse" class="xs3p-panel-title collapsed">Schema Component Representation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

    <element name="interchange">
       <complexType>
          <complexContent>
             <extension base="tns:controlType">
                <sequence>
                   <element name="sequence">
                      <complexType>
                         <sequence>
                            <element name="segment" type="tns:segmentStandard" minOccurs="0" maxOccurs="unbounded"/>
                            <element name="group" type="tns:groupControlType" minOccurs="0"/>
                            <element name="transaction" type="tns:transactionControlType" minOccurs="0"/>
                         </sequence>
                      </complexType>
                   </element>
                   <element ref="tns:syntax" minOccurs="0" maxOccurs="unbounded"/>
                </sequence>
             </extension>
          </complexContent>
       </complexType>
    </element>

[<span class="glyphicon glyphicon-chevron-up">
</span>](#top "Go to top of page")

------------------------------------------------------------------------

### Element: <span id="element_schema" class="name">schema</span>

#### <a href="#element_schema-properties-table-collapse" class="xs3p-panel-title">Properties</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

<table class="table table-striped xs3p-in-panel-table">
<tbody>
<tr class="odd">
<td>Name</td>
<td>schema</td>
</tr>
<tr class="even">
<td>Type</td>
<td>Locally-defined complex type</td>
</tr>
<tr class="odd">
<td><a href="#term_Nillable" title="Look up &#39;Nillable&#39; in glossary">Nillable</a></td>
<td>no</td>
</tr>
<tr class="even">
<td><a href="#term_Abstract" title="Look up &#39;Abstract&#39; in glossary">Abstract</a></td>
<td>no</td>
</tr>
</tbody>
</table>

#### <a href="#element_schema-doc-panel-collapse" class="xs3p-panel-title">Documentation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

No documentation provided.

#### <a href="#element_schema-instance-table-collapse" class="xs3p-panel-title">XML Instance Representation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

    <tns:schema>
    ×Element includeOptional reference to another schema file to include. Close   <tns:include> ... </tns:include> [0..*]  
       Start Choice [0..1]
          <tns:interchange> ... </tns:interchange> [1]
          <tns:transaction> ... </tns:transaction> [1]
          <tns:implementation> ... </tns:implementation> [0..1]
          <tns:implementation> ... </tns:implementation> [1]
       End Choice
       Start Choice [1..*]
          <tns:elementType> ... </tns:elementType> [1..*]
          <tns:compositeType> ... </tns:compositeType> [0..*]
          <tns:segmentType> ... </tns:segmentType> [1..*]
       End Choice
    </tns:schema>

#### <a href="#element_schema-schemaComponent-collapse" class="xs3p-panel-title collapsed">Schema Component Representation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

    <element name="schema">
       <complexType>
          <sequence>
             <element ref="tns:include" minOccurs="0" maxOccurs="unbounded"/>
             <choice minOccurs="0">
                <element ref="tns:interchange"/>
                <sequence>
                   <element ref="tns:transaction"/>
                   <element ref="tns:implementation" minOccurs="0"/>
                </sequence>
                <sequence>
                   <element ref="tns:implementation"/>
                </sequence>
             </choice>
             <choice id="typeChoice" maxOccurs="unbounded">
                <element ref="tns:elementType" maxOccurs="unbounded"/>
                <element ref="tns:compositeType" minOccurs="0" maxOccurs="unbounded"/>
                <element ref="tns:segmentType" maxOccurs="unbounded"/>
             </choice>
          </sequence>
       </complexType>
    </element>

[<span class="glyphicon glyphicon-chevron-up">
</span>](#top "Go to top of page")

------------------------------------------------------------------------

### Element: <span id="element_segmentType" class="name">segmentType</span>

#### <a href="#element_segmentType-properties-table-collapse" class="xs3p-panel-title">Properties</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

<table class="table table-striped xs3p-in-panel-table">
<tbody>
<tr class="odd">
<td>Name</td>
<td>segmentType</td>
</tr>
<tr class="even">
<td>Type</td>
<td>Locally-defined complex type</td>
</tr>
<tr class="odd">
<td><a href="#term_Nillable" title="Look up &#39;Nillable&#39; in glossary">Nillable</a></td>
<td>no</td>
</tr>
<tr class="even">
<td><a href="#term_Abstract" title="Look up &#39;Abstract&#39; in glossary">Abstract</a></td>
<td>no</td>
</tr>
</tbody>
</table>

#### <a href="#element_segmentType-doc-panel-collapse" class="xs3p-panel-title">Documentation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

Used to declare a segment

#### <a href="#element_segmentType-instance-table-collapse" class="xs3p-panel-title">XML Instance Representation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

    <tns:segmentType
     title="string" [0..1]
     name="tns:nameType (length <= 3)" [1]×Attribute name
                    Name of the segment. Also referred to as the segment's tag. This is the two or three
                    character string used to identify a segment.
                   Close  
    >
       <tns:description> ... </tns:description> [0..1]
       <tns:sequence   > [0..1]   
          Start Choice [0..*]
             <tns:element> tns:elementStandard </tns:element> [1]  
             <tns:composite> tns:compositeStandard </tns:composite> [1]
             <tns:any> tns:anyElementType </tns:any> [1]  
          End Choice
       </tns:sequence>
       <tns:syntax> ... </tns:syntax> [0..*]
    </tns:segmentType>

#### <a href="#element_segmentType-schemaComponent-collapse" class="xs3p-panel-title collapsed">Schema Component Representation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

    <element name="segmentType">
       <complexType>
          <complexContent>
             <extension base="tns:baseType">
                <sequence>
                   <element name="sequence" minOccurs="0">
                      <complexType>
                         <choice minOccurs="0" maxOccurs="unbounded">
                            <element name="element" type="tns:elementStandard"/>
                            <element name="composite" type="tns:compositeStandard"/>
                            <element name="any" type="tns:anyElementType"/>
                         </choice>
                      </complexType>
                   </element>
                   <element ref="tns:syntax" minOccurs="0" maxOccurs="unbounded"/>
                </sequence>
                <attribute name="name" use="required">
                   <simpleType>
                      <restriction base="tns:nameType">
                         <maxLength value="3"/>
                      </restriction>
                   </simpleType>
                </attribute>
             </extension>
          </complexContent>
       </complexType>
    </element>

[<span class="glyphicon glyphicon-chevron-up">
</span>](#top "Go to top of page")

------------------------------------------------------------------------

### Element: <span id="element_syntax" class="name">syntax</span>

#### <a href="#element_syntax-properties-table-collapse" class="xs3p-panel-title">Properties</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

<table class="table table-striped xs3p-in-panel-table">
<tbody>
<tr class="odd">
<td>Name</td>
<td>syntax</td>
</tr>
<tr class="even">
<td>Type</td>
<td>Locally-defined complex type</td>
</tr>
<tr class="odd">
<td><a href="#term_Nillable" title="Look up &#39;Nillable&#39; in glossary">Nillable</a></td>
<td>no</td>
</tr>
<tr class="even">
<td><a href="#term_Abstract" title="Look up &#39;Abstract&#39; in glossary">Abstract</a></td>
<td>no</td>
</tr>
</tbody>
</table>

#### <a href="#element_syntax-doc-panel-collapse" class="xs3p-panel-title">Documentation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

No documentation provided.

#### <a href="#element_syntax-instance-table-collapse" class="xs3p-panel-title">XML Instance Representation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

    <tns:syntax
     type="tns:syntaxType" [0..1]
    >
       <tns:position> tns:positionType </tns:position> [1..*]
    </tns:syntax>

#### <a href="#element_syntax-schemaComponent-collapse" class="xs3p-panel-title collapsed">Schema Component Representation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

    <element name="syntax">
       <complexType>
          <sequence>
             <element name="position" type="tns:positionType" maxOccurs="unbounded"/>
          </sequence>
          <attribute name="type" type="tns:syntaxType"/>
       </complexType>
    </element>

[<span class="glyphicon glyphicon-chevron-up">
</span>](#top "Go to top of page")

------------------------------------------------------------------------

### Element: <span id="element_transaction" class="name">transaction</span>

#### <a href="#element_transaction-properties-table-collapse" class="xs3p-panel-title">Properties</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

<table class="table table-striped xs3p-in-panel-table">
<tbody>
<tr class="odd">
<td>Name</td>
<td>transaction</td>
</tr>
<tr class="even">
<td>Type</td>
<td>Locally-defined complex type</td>
</tr>
<tr class="odd">
<td><a href="#term_Nillable" title="Look up &#39;Nillable&#39; in glossary">Nillable</a></td>
<td>no</td>
</tr>
<tr class="even">
<td><a href="#term_Abstract" title="Look up &#39;Abstract&#39; in glossary">Abstract</a></td>
<td>no</td>
</tr>
</tbody>
</table>

#### <a href="#element_transaction-doc-panel-collapse" class="xs3p-panel-title">Documentation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

No documentation provided.

#### <a href="#element_transaction-instance-table-collapse" class="xs3p-panel-title">XML Instance Representation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

    <tns:transaction
     title="string" [0..1]
    >
       <tns:description> ... </tns:description> [0..1]
       <tns:sequence   > [1]   
          Start Choice [1..*]
             <tns:segment> tns:segmentStandard </tns:segment> [1]
             <tns:loop> tns:loopStandard </tns:loop> [0..1]
          End Choice
       </tns:sequence>
       <tns:syntax> ... </tns:syntax> [0..*]
    </tns:transaction>

#### <a href="#element_transaction-schemaComponent-collapse" class="xs3p-panel-title collapsed">Schema Component Representation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

    <element name="transaction">
       <complexType>
          <complexContent>
             <extension base="tns:baseType">
                <sequence>
                   <element name="sequence">
                      <complexType>
                         <choice maxOccurs="unbounded">
                            <element name="segment" type="tns:segmentStandard"/>
                            <element name="loop" type="tns:loopStandard" minOccurs="0"/>
                         </choice>
                      </complexType>
                   </element>
                   <element ref="tns:syntax" minOccurs="0" maxOccurs="unbounded"/>
                </sequence>
             </extension>
          </complexContent>
       </complexType>
    </element>

[<span class="glyphicon glyphicon-chevron-up">
</span>](#top "Go to top of page")

------------------------------------------------------------------------

<span id="SchemaDefinitions">Global Definitions</span>
------------------------------------------------------

### Attribute Group: <span id="attributeGroup_implementationAttributeGroup" class="name">implementationAttributeGroup</span>

#### <a href="#attributeGroup_implementationAttributeGroup-properties-table-collapse" class="xs3p-panel-title">Properties</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

<table class="table tables-striped xs3p-in-panel-table">
<tbody>
<tr class="odd">
<td>Name</td>
<td>implementationAttributeGroup</td>
</tr>
</tbody>
</table>

#### <a href="#attributeGroup_implementationAttributeGroup-doc-panel-collapse" class="xs3p-panel-title">Documentation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

No documentation provided.

#### <a href="#attributeGroup_implementationAttributeGroup-instance-table-collapse" class="xs3p-panel-title">XML Instance Representation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

    minOccurs="nonNegativeInteger" [0..1]×Attribute minOccurs
              The minimum number of times a type may occur at the declared location
              in the EDI structure.
             Close  
    maxOccurs="nonNegativeInteger" [0..1]×Attribute maxOccurs
              The maximum number of times a type may occur at the declared location
              in the EDI structure.
             Close  

#### <a href="#attributeGroup_implementationAttributeGroup-schemaComponent-collapse" class="xs3p-panel-title collapsed">Schema Component Representation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

    <attributeGroup name="implementationAttributeGroup">
       <attribute name="minOccurs" type="nonNegativeInteger"/>
       <attribute name="maxOccurs" type="nonNegativeInteger"/>
    </attributeGroup>

[<span class="glyphicon glyphicon-chevron-up">
</span>](#top "Go to top of page")

------------------------------------------------------------------------

### Attribute Group: <span id="attributeGroup_lengthAttributeGroup" class="name">lengthAttributeGroup</span>

#### <a href="#attributeGroup_lengthAttributeGroup-properties-table-collapse" class="xs3p-panel-title">Properties</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

<table class="table tables-striped xs3p-in-panel-table">
<tbody>
<tr class="odd">
<td>Name</td>
<td>lengthAttributeGroup</td>
</tr>
</tbody>
</table>

#### <a href="#attributeGroup_lengthAttributeGroup-doc-panel-collapse" class="xs3p-panel-title">Documentation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

No documentation provided.

#### <a href="#attributeGroup_lengthAttributeGroup-instance-table-collapse" class="xs3p-panel-title">XML Instance Representation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

    minLength="nonNegativeInteger" [0..1]×Attribute minLength
              The minimum length allowed for an element value to be valid.
             Close  
    maxLength="nonNegativeInteger" [0..1]×Attribute maxLength
              The maximum length allowed for an element value to be valid.
             Close  

#### <a href="#attributeGroup_lengthAttributeGroup-schemaComponent-collapse" class="xs3p-panel-title collapsed">Schema Component Representation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

    <attributeGroup name="lengthAttributeGroup">
       <attribute name="minLength" type="nonNegativeInteger" default="1"/>
       <attribute name="maxLength" type="nonNegativeInteger" default="1"/>
    </attributeGroup>

[<span class="glyphicon glyphicon-chevron-up">
</span>](#top "Go to top of page")

------------------------------------------------------------------------

### Attribute Group: <span id="attributeGroup_occursAttributeGroup" class="name">occursAttributeGroup</span>

#### <a href="#attributeGroup_occursAttributeGroup-properties-table-collapse" class="xs3p-panel-title">Properties</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

<table class="table tables-striped xs3p-in-panel-table">
<tbody>
<tr class="odd">
<td>Name</td>
<td>occursAttributeGroup</td>
</tr>
</tbody>
</table>

#### <a href="#attributeGroup_occursAttributeGroup-doc-panel-collapse" class="xs3p-panel-title">Documentation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

No documentation provided.

#### <a href="#attributeGroup_occursAttributeGroup-instance-table-collapse" class="xs3p-panel-title">XML Instance Representation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

    minOccurs="nonNegativeInteger" [0..1]×Attribute minOccurs
              The minimum number of times a type may occur at the declared location
              in the EDI structure.
             Close  
    maxOccurs="nonNegativeInteger" [0..1]×Attribute maxOccurs
              The maximum number of times a type may occur at the declared location
              in the EDI structure.
             Close  

#### <a href="#attributeGroup_occursAttributeGroup-schemaComponent-collapse" class="xs3p-panel-title collapsed">Schema Component Representation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

    <attributeGroup name="occursAttributeGroup">
       <attribute name="minOccurs" type="nonNegativeInteger" default="0"/>
       <attribute name="maxOccurs" type="nonNegativeInteger" default="1"/>
    </attributeGroup>

[<span class="glyphicon glyphicon-chevron-up">
</span>](#top "Go to top of page")

------------------------------------------------------------------------

### Attribute Group: <span id="attributeGroup_referenceAttributeGroup" class="name">referenceAttributeGroup</span>

#### <a href="#attributeGroup_referenceAttributeGroup-properties-table-collapse" class="xs3p-panel-title">Properties</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

<table class="table tables-striped xs3p-in-panel-table">
<tbody>
<tr class="odd">
<td>Name</td>
<td>referenceAttributeGroup</td>
</tr>
</tbody>
</table>

#### <a href="#attributeGroup_referenceAttributeGroup-doc-panel-collapse" class="xs3p-panel-title">Documentation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

No documentation provided.

#### <a href="#attributeGroup_referenceAttributeGroup-instance-table-collapse" class="xs3p-panel-title">XML Instance Representation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

    type="NCName" [0..1]×Attribute type
              The name of the target type being referenced.
             Close  
    minOccurs="nonNegativeInteger" [0..1]×Attribute minOccurs
              The minimum number of times a type may occur at the declared location
              in the EDI structure.
             Close  
    maxOccurs="nonNegativeInteger" [0..1]×Attribute maxOccurs
              The maximum number of times a type may occur at the declared location
              in the EDI structure.
             Close  

#### <a href="#attributeGroup_referenceAttributeGroup-schemaComponent-collapse" class="xs3p-panel-title collapsed">Schema Component Representation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

    <attributeGroup name="referenceAttributeGroup">
       <attribute name="type" type="NCName"/>
       <attributeGroup ref="tns:occursAttributeGroup"/>
    </attributeGroup>

[<span class="glyphicon glyphicon-chevron-up">
</span>](#top "Go to top of page")

------------------------------------------------------------------------

### Attribute Group: <span id="attributeGroup_versionAttributeGroup" class="name">versionAttributeGroup</span>

#### <a href="#attributeGroup_versionAttributeGroup-properties-table-collapse" class="xs3p-panel-title">Properties</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

<table class="table tables-striped xs3p-in-panel-table">
<tbody>
<tr class="odd">
<td>Name</td>
<td>versionAttributeGroup</td>
</tr>
</tbody>
</table>

#### <a href="#attributeGroup_versionAttributeGroup-doc-panel-collapse" class="xs3p-panel-title">Documentation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

No documentation provided.

#### <a href="#attributeGroup_versionAttributeGroup-instance-table-collapse" class="xs3p-panel-title">XML Instance Representation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

    minVersion="token" [0..1]×Attribute minVersion
              The minimum transaction version this schema version applies to.
             Close  
    maxVersion="token" [0..1]×Attribute maxVersion
              The maximum transaction version this schema version applies to.
             Close  

#### <a href="#attributeGroup_versionAttributeGroup-schemaComponent-collapse" class="xs3p-panel-title collapsed">Schema Component Representation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

    <attributeGroup name="versionAttributeGroup">
       <attribute name="minVersion" type="token"/>
       <attribute name="maxVersion" type="token"/>
    </attributeGroup>

[<span class="glyphicon glyphicon-chevron-up">
</span>](#top "Go to top of page")

------------------------------------------------------------------------

### Complex Type: <span id="type_anyElementType" class="name">anyElementType</span>

#### <a href="#type_anyElementType-type-hierarchy-collapse" class="xs3p-panel-title">Type hierarchy</a>

<table class="table table-striped xs3p-in-panel-table">
<tbody>
<tr class="odd">
<td>Super-types:</td>
<td><span class="type"><a href="#type_baseType" title="Jump to &quot;baseType&quot; type definition.">baseType</a></span> &lt; <strong>anyElementType</strong> (by extension)</td>
</tr>
<tr class="even">
<td>Sub-types:</td>
<td>None</td>
</tr>
</tbody>
</table>

#### <a href="#type_anyElementType-properties-table-collapse" class="xs3p-panel-title">Properties</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

<table class="table table-striped xs3p-in-panel-table">
<tbody>
<tr class="odd">
<td>Name</td>
<td>anyElementType</td>
</tr>
<tr class="even">
<td><a href="#term_Abstract" title="Look up &#39;Abstract&#39; in glossary">Abstract</a></td>
<td>no</td>
</tr>
</tbody>
</table>

#### <a href="#type_anyElementType-doc-panel-collapse" class="xs3p-panel-title">Documentation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

No documentation provided.

#### <a href="#type_anyElementType-instance-table-collapse" class="xs3p-panel-title">XML Instance Representation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

    <...
     title="string" [0..1]
     minOccurs="nonNegativeInteger" [0..1]×Attribute minOccursThe minimum number of times an undefined element may occur at the declared location in the EDI structure. Close  
     maxOccurs="nonNegativeInteger" [0..1]×Attribute maxOccursThe maximum number of times an undefined element may occur at the declared location in the EDI structure. Close  
    >
       <tns:description> ... </tns:description> [0..1]
    </...>

#### <a href="#type_anyElementType-schemaComponent-collapse" class="xs3p-panel-title collapsed">Schema Component Representation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

    <complexType name="anyElementType">
       <complexContent>
          <extension base="tns:baseType">
             <attribute name="minOccurs" type="nonNegativeInteger" default="0"/>
             <attribute name="maxOccurs" type="nonNegativeInteger" default="1"/>
          </extension>
       </complexContent>
    </complexType>

[<span class="glyphicon glyphicon-chevron-up">
</span>](#top "Go to top of page")

------------------------------------------------------------------------

### Complex Type: <span id="type_baseType" class="name">baseType</span>

#### <a href="#type_baseType-type-hierarchy-collapse" class="xs3p-panel-title">Type hierarchy</a>

<table class="table table-striped xs3p-in-panel-table">
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Super-types:</td>
<td>None</td>
</tr>
<tr class="even">
<td>Sub-types:</td>
<td><ul class="incremental">
<li><span class="type"><a href="#type_anyElementType" title="Jump to &quot;anyElementType&quot; type definition.">anyElementType</a></span> (by extension)</li>
<li><span class="type"><a href="#type_controlType" title="Jump to &quot;controlType&quot; type definition.">controlType</a></span> (by extension)
<ul class="incremental">
<li><span class="type"><a href="#type_transactionControlType" title="Jump to &quot;transactionControlType&quot; type definition.">transactionControlType</a></span> (by extension)</li>
<li><span class="type"><a href="#type_groupControlType" title="Jump to &quot;groupControlType&quot; type definition.">groupControlType</a></span> (by extension)</li>
</ul></li>
<li><span class="type"><a href="#type_elementStandard" title="Jump to &quot;elementStandard&quot; type definition.">elementStandard</a></span> (by extension)</li>
<li><span class="type"><a href="#type_elementImpl" title="Jump to &quot;elementImpl&quot; type definition.">elementImpl</a></span> (by extension)</li>
<li><span class="type"><a href="#type_compositeStandard" title="Jump to &quot;compositeStandard&quot; type definition.">compositeStandard</a></span> (by extension)</li>
<li><span class="type"><a href="#type_compositeImpl" title="Jump to &quot;compositeImpl&quot; type definition.">compositeImpl</a></span> (by extension)</li>
<li><span class="type"><a href="#type_segmentStandard" title="Jump to &quot;segmentStandard&quot; type definition.">segmentStandard</a></span> (by extension)</li>
<li><span class="type"><a href="#type_segmentImpl" title="Jump to &quot;segmentImpl&quot; type definition.">segmentImpl</a></span> (by extension)</li>
<li><span class="type"><a href="#type_loopBase" title="Jump to &quot;loopBase&quot; type definition.">loopBase</a></span> (by extension)
<ul class="incremental">
<li><span class="type"><a href="#type_loopStandard" title="Jump to &quot;loopStandard&quot; type definition.">loopStandard</a></span> (by extension)</li>
<li><span class="type"><a href="#type_loopImpl" title="Jump to &quot;loopImpl&quot; type definition.">loopImpl</a></span> (by extension)</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>

#### <a href="#type_baseType-properties-table-collapse" class="xs3p-panel-title">Properties</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

<table class="table table-striped xs3p-in-panel-table">
<tbody>
<tr class="odd">
<td>Name</td>
<td>baseType</td>
</tr>
<tr class="even">
<td><a href="#term_Abstract" title="Look up &#39;Abstract&#39; in glossary">Abstract</a></td>
<td>yes</td>
</tr>
</tbody>
</table>

#### <a href="#type_baseType-doc-panel-collapse" class="xs3p-panel-title">Documentation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

No documentation provided.

#### <a href="#type_baseType-instance-table-collapse" class="xs3p-panel-title">XML Instance Representation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

    <...
     title="string" [0..1]
    >
       <tns:description> ... </tns:description> [0..1]
    </...>

#### <a href="#type_baseType-schemaComponent-collapse" class="xs3p-panel-title collapsed">Schema Component Representation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

    <complexType name="baseType" abstract="true">
       <sequence>
          <element ref="tns:description" minOccurs="0" maxOccurs="1"/>
       </sequence>
       <attribute name="title" type="string" use="optional"/>
    </complexType>

[<span class="glyphicon glyphicon-chevron-up">
</span>](#top "Go to top of page")

------------------------------------------------------------------------

### Complex Type: <span id="type_compositeImpl" class="name">compositeImpl</span>

#### <a href="#type_compositeImpl-type-hierarchy-collapse" class="xs3p-panel-title">Type hierarchy</a>

<table class="table table-striped xs3p-in-panel-table">
<tbody>
<tr class="odd">
<td>Super-types:</td>
<td><span class="type"><a href="#type_baseType" title="Jump to &quot;baseType&quot; type definition.">baseType</a></span> &lt; <strong>compositeImpl</strong> (by extension)</td>
</tr>
<tr class="even">
<td>Sub-types:</td>
<td>None</td>
</tr>
</tbody>
</table>

#### <a href="#type_compositeImpl-properties-table-collapse" class="xs3p-panel-title">Properties</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

<table class="table table-striped xs3p-in-panel-table">
<tbody>
<tr class="odd">
<td>Name</td>
<td>compositeImpl</td>
</tr>
<tr class="even">
<td><a href="#term_Abstract" title="Look up &#39;Abstract&#39; in glossary">Abstract</a></td>
<td>no</td>
</tr>
</tbody>
</table>

#### <a href="#type_compositeImpl-doc-panel-collapse" class="xs3p-panel-title">Documentation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

No documentation provided.

#### <a href="#type_compositeImpl-instance-table-collapse" class="xs3p-panel-title">XML Instance Representation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

    <...
     title="string" [0..1]
     position="tns:positionType" [1]
     minOccurs="nonNegativeInteger" [0..1]×Attribute minOccurs
              The minimum number of times a type may occur at the declared location
              in the EDI structure.
             Close  
     maxOccurs="nonNegativeInteger" [0..1]×Attribute maxOccurs
              The maximum number of times a type may occur at the declared location
              in the EDI structure.
             Close  
    >
       <tns:description> ... </tns:description> [0..1]
       <tns:sequence   > [0..1]   
          <tns:element> tns:elementImpl </tns:element> [1..*]
       </tns:sequence>
    </...>

#### <a href="#type_compositeImpl-schemaComponent-collapse" class="xs3p-panel-title collapsed">Schema Component Representation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

    <complexType name="compositeImpl">
       <complexContent>
          <extension base="tns:baseType">
             <sequence>
                <element name="sequence" minOccurs="0">
                   <complexType>
                      <sequence>
                         <element name="element" type="tns:elementImpl" minOccurs="1" maxOccurs="unbounded"/>
                      </sequence>
                   </complexType>
                </element>
             </sequence>
             <attribute name="position" type="tns:positionType" use="required"/>
             <attributeGroup ref="tns:implementationAttributeGroup"/>
          </extension>
       </complexContent>
    </complexType>

[<span class="glyphicon glyphicon-chevron-up">
</span>](#top "Go to top of page")

------------------------------------------------------------------------

### Complex Type: <span id="type_compositeStandard" class="name">compositeStandard</span>

#### <a href="#type_compositeStandard-type-hierarchy-collapse" class="xs3p-panel-title">Type hierarchy</a>

<table class="table table-striped xs3p-in-panel-table">
<tbody>
<tr class="odd">
<td>Super-types:</td>
<td><span class="type"><a href="#type_baseType" title="Jump to &quot;baseType&quot; type definition.">baseType</a></span> &lt; <strong>compositeStandard</strong> (by extension)</td>
</tr>
<tr class="even">
<td>Sub-types:</td>
<td>None</td>
</tr>
</tbody>
</table>

#### <a href="#type_compositeStandard-properties-table-collapse" class="xs3p-panel-title">Properties</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

<table class="table table-striped xs3p-in-panel-table">
<tbody>
<tr class="odd">
<td>Name</td>
<td>compositeStandard</td>
</tr>
<tr class="even">
<td><a href="#term_Abstract" title="Look up &#39;Abstract&#39; in glossary">Abstract</a></td>
<td>no</td>
</tr>
</tbody>
</table>

#### <a href="#type_compositeStandard-doc-panel-collapse" class="xs3p-panel-title">Documentation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

No documentation provided.

#### <a href="#type_compositeStandard-instance-table-collapse" class="xs3p-panel-title">XML Instance Representation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

    <...
     title="string" [0..1]
     type="NCName" [0..1]×Attribute type
              The name of the target type being referenced.
             Close  
     minOccurs="nonNegativeInteger" [0..1]×Attribute minOccurs
              The minimum number of times a type may occur at the declared location
              in the EDI structure.
             Close  
     maxOccurs="nonNegativeInteger" [0..1]×Attribute maxOccurs
              The maximum number of times a type may occur at the declared location
              in the EDI structure.
             Close  
    >
       <tns:description> ... </tns:description> [0..1]
       <tns:version
        minVersion="token" [0..1]×Attribute minVersion
              The minimum transaction version this schema version applies to.
             Close  
        maxVersion="token" [0..1]×Attribute maxVersion
              The maximum transaction version this schema version applies to.
             Close  
        minOccurs="nonNegativeInteger" [0..1]×Attribute minOccurs
              The minimum number of times a type may occur at the declared location
              in the EDI structure.
             Close  
        maxOccurs="nonNegativeInteger" [0..1]×Attribute maxOccurs
              The maximum number of times a type may occur at the declared location
              in the EDI structure.
             Close  
    />  [0..*]

    </...>

#### <a href="#type_compositeStandard-schemaComponent-collapse" class="xs3p-panel-title collapsed">Schema Component Representation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

    <complexType name="compositeStandard">
       <complexContent>
          <extension base="tns:baseType">
             <sequence>
                <element name="version" minOccurs="0" maxOccurs="unbounded">
                   <complexType>
                      <attributeGroup ref="tns:versionAttributeGroup"/>
                      <attributeGroup ref="tns:occursAttributeGroup"/>
                   </complexType>
                </element>
             </sequence>
             <attributeGroup ref="tns:referenceAttributeGroup"/>
          </extension>
       </complexContent>
    </complexType>

[<span class="glyphicon glyphicon-chevron-up">
</span>](#top "Go to top of page")

------------------------------------------------------------------------

### Complex Type: <span id="type_controlType" class="name">controlType</span>

#### <a href="#type_controlType-type-hierarchy-collapse" class="xs3p-panel-title">Type hierarchy</a>

<table class="table table-striped xs3p-in-panel-table">
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Super-types:</td>
<td><span class="type"><a href="#type_baseType" title="Jump to &quot;baseType&quot; type definition.">baseType</a></span> &lt; <strong>controlType</strong> (by extension)</td>
</tr>
<tr class="even">
<td>Sub-types:</td>
<td><ul class="incremental">
<li><span class="type"><a href="#type_transactionControlType" title="Jump to &quot;transactionControlType&quot; type definition.">transactionControlType</a></span> (by extension)</li>
<li><span class="type"><a href="#type_groupControlType" title="Jump to &quot;groupControlType&quot; type definition.">groupControlType</a></span> (by extension)</li>
</ul></td>
</tr>
</tbody>
</table>

#### <a href="#type_controlType-properties-table-collapse" class="xs3p-panel-title">Properties</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

<table class="table table-striped xs3p-in-panel-table">
<tbody>
<tr class="odd">
<td>Name</td>
<td>controlType</td>
</tr>
<tr class="even">
<td><a href="#term_Abstract" title="Look up &#39;Abstract&#39; in glossary">Abstract</a></td>
<td>yes</td>
</tr>
</tbody>
</table>

#### <a href="#type_controlType-doc-panel-collapse" class="xs3p-panel-title">Documentation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

No documentation provided.

#### <a href="#type_controlType-instance-table-collapse" class="xs3p-panel-title">XML Instance Representation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

    <...
     title="string" [0..1]
     header="NCName" [1]
     trailer="NCName" [1]
    >
       <tns:description> ... </tns:description> [0..1]
    </...>

#### <a href="#type_controlType-schemaComponent-collapse" class="xs3p-panel-title collapsed">Schema Component Representation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

    <complexType name="controlType" abstract="true">
       <complexContent>
          <extension base="tns:baseType">
             <attribute name="header" type="NCName" use="required"/>
             <attribute name="trailer" type="NCName" use="required"/>
          </extension>
       </complexContent>
    </complexType>

[<span class="glyphicon glyphicon-chevron-up">
</span>](#top "Go to top of page")

------------------------------------------------------------------------

### Complex Type: <span id="type_elementImpl" class="name">elementImpl</span>

#### <a href="#type_elementImpl-type-hierarchy-collapse" class="xs3p-panel-title">Type hierarchy</a>

<table class="table table-striped xs3p-in-panel-table">
<tbody>
<tr class="odd">
<td>Super-types:</td>
<td><span class="type"><a href="#type_baseType" title="Jump to &quot;baseType&quot; type definition.">baseType</a></span> &lt; <strong>elementImpl</strong> (by extension)</td>
</tr>
<tr class="even">
<td>Sub-types:</td>
<td>None</td>
</tr>
</tbody>
</table>

#### <a href="#type_elementImpl-properties-table-collapse" class="xs3p-panel-title">Properties</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

<table class="table table-striped xs3p-in-panel-table">
<tbody>
<tr class="odd">
<td>Name</td>
<td>elementImpl</td>
</tr>
<tr class="even">
<td><a href="#term_Abstract" title="Look up &#39;Abstract&#39; in glossary">Abstract</a></td>
<td>no</td>
</tr>
</tbody>
</table>

#### <a href="#type_elementImpl-doc-panel-collapse" class="xs3p-panel-title">Documentation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

No documentation provided.

#### <a href="#type_elementImpl-instance-table-collapse" class="xs3p-panel-title">XML Instance Representation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

    <...
     title="string" [0..1]
     position="tns:positionType" [1]
     minOccurs="nonNegativeInteger" [0..1]×Attribute minOccurs
              The minimum number of times a type may occur at the declared location
              in the EDI structure.
             Close  
     maxOccurs="nonNegativeInteger" [0..1]×Attribute maxOccurs
              The maximum number of times a type may occur at the declared location
              in the EDI structure.
             Close  
    >
       <tns:description> ... </tns:description> [0..1]
       <tns:enumeration> ... </tns:enumeration> [0..1]
    </...>

#### <a href="#type_elementImpl-schemaComponent-collapse" class="xs3p-panel-title collapsed">Schema Component Representation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

    <complexType name="elementImpl">
       <complexContent>
          <extension base="tns:baseType">
             <sequence>
                <element ref="tns:enumeration" minOccurs="0"/>
             </sequence>
             <attribute name="position" type="tns:positionType" use="required"/>
             <attributeGroup ref="tns:implementationAttributeGroup"/>
          </extension>
       </complexContent>
    </complexType>

[<span class="glyphicon glyphicon-chevron-up">
</span>](#top "Go to top of page")

------------------------------------------------------------------------

### Complex Type: <span id="type_elementStandard" class="name">elementStandard</span>

#### <a href="#type_elementStandard-type-hierarchy-collapse" class="xs3p-panel-title">Type hierarchy</a>

<table class="table table-striped xs3p-in-panel-table">
<tbody>
<tr class="odd">
<td>Super-types:</td>
<td><span class="type"><a href="#type_baseType" title="Jump to &quot;baseType&quot; type definition.">baseType</a></span> &lt; <strong>elementStandard</strong> (by extension)</td>
</tr>
<tr class="even">
<td>Sub-types:</td>
<td>None</td>
</tr>
</tbody>
</table>

#### <a href="#type_elementStandard-properties-table-collapse" class="xs3p-panel-title">Properties</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

<table class="table table-striped xs3p-in-panel-table">
<tbody>
<tr class="odd">
<td>Name</td>
<td>elementStandard</td>
</tr>
<tr class="even">
<td><a href="#term_Abstract" title="Look up &#39;Abstract&#39; in glossary">Abstract</a></td>
<td>no</td>
</tr>
</tbody>
</table>

#### <a href="#type_elementStandard-doc-panel-collapse" class="xs3p-panel-title">Documentation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

No documentation provided.

#### <a href="#type_elementStandard-instance-table-collapse" class="xs3p-panel-title">XML Instance Representation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

    <...
     title="string" [0..1]
     type="NCName" [0..1]×Attribute type
              The name of the target type being referenced.
             Close  
     minOccurs="nonNegativeInteger" [0..1]×Attribute minOccurs
              The minimum number of times a type may occur at the declared location
              in the EDI structure.
             Close  
     maxOccurs="nonNegativeInteger" [0..1]×Attribute maxOccurs
              The maximum number of times a type may occur at the declared location
              in the EDI structure.
             Close  
    >
       <tns:description> ... </tns:description> [0..1]
       <tns:version
        minVersion="token" [0..1]×Attribute minVersion
              The minimum transaction version this schema version applies to.
             Close  
        maxVersion="token" [0..1]×Attribute maxVersion
              The maximum transaction version this schema version applies to.
             Close  
        minOccurs="nonNegativeInteger" [0..1]×Attribute minOccurs
              The minimum number of times a type may occur at the declared location
              in the EDI structure.
             Close  
        maxOccurs="nonNegativeInteger" [0..1]×Attribute maxOccurs
              The maximum number of times a type may occur at the declared location
              in the EDI structure.
             Close  
    />  [0..*]

    </...>

#### <a href="#type_elementStandard-schemaComponent-collapse" class="xs3p-panel-title collapsed">Schema Component Representation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

    <complexType name="elementStandard">
       <complexContent>
          <extension base="tns:baseType">
             <sequence>
                <element name="version" minOccurs="0" maxOccurs="unbounded">
                   <complexType>
                      <attributeGroup ref="tns:versionAttributeGroup"/>
                      <attributeGroup ref="tns:occursAttributeGroup"/>
                   </complexType>
                </element>
             </sequence>
             <attributeGroup ref="tns:referenceAttributeGroup"/>
          </extension>
       </complexContent>
    </complexType>

[<span class="glyphicon glyphicon-chevron-up">
</span>](#top "Go to top of page")

------------------------------------------------------------------------

### Complex Type: <span id="type_groupControlType" class="name">groupControlType</span>

#### <a href="#type_groupControlType-type-hierarchy-collapse" class="xs3p-panel-title">Type hierarchy</a>

<table class="table table-striped xs3p-in-panel-table">
<tbody>
<tr class="odd">
<td>Super-types:</td>
<td><span class="type"><a href="#type_baseType" title="Jump to &quot;baseType&quot; type definition.">baseType</a></span> &lt; <span class="type"><a href="#type_controlType" title="Jump to &quot;controlType&quot; type definition.">controlType</a></span> (by extension) &lt; <strong>groupControlType</strong> (by extension)</td>
</tr>
<tr class="even">
<td>Sub-types:</td>
<td>None</td>
</tr>
</tbody>
</table>

#### <a href="#type_groupControlType-properties-table-collapse" class="xs3p-panel-title">Properties</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

<table class="table table-striped xs3p-in-panel-table">
<tbody>
<tr class="odd">
<td>Name</td>
<td>groupControlType</td>
</tr>
<tr class="even">
<td><a href="#term_Abstract" title="Look up &#39;Abstract&#39; in glossary">Abstract</a></td>
<td>no</td>
</tr>
</tbody>
</table>

#### <a href="#type_groupControlType-doc-panel-collapse" class="xs3p-panel-title">Documentation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

No documentation provided.

#### <a href="#type_groupControlType-instance-table-collapse" class="xs3p-panel-title">XML Instance Representation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

    <...
     title="string" [0..1]
     header="NCName" [1]
     trailer="NCName" [1]
     use="tns:useType" [0..1]
    >
       <tns:description> ... </tns:description> [0..1]
       <tns:transaction> tns:transactionControlType </tns:transaction> [0..1]
    </...>

#### <a href="#type_groupControlType-schemaComponent-collapse" class="xs3p-panel-title collapsed">Schema Component Representation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

    <complexType name="groupControlType">
       <complexContent>
          <extension base="tns:controlType">
             <sequence>
                <element name="transaction" type="tns:transactionControlType" minOccurs="0"/>
             </sequence>
             <attribute name="use" type="tns:useType" default="optional"/>
          </extension>
       </complexContent>
    </complexType>

[<span class="glyphicon glyphicon-chevron-up">
</span>](#top "Go to top of page")

------------------------------------------------------------------------

### Complex Type: <span id="type_loopBase" class="name">loopBase</span>

#### <a href="#type_loopBase-type-hierarchy-collapse" class="xs3p-panel-title">Type hierarchy</a>

<table class="table table-striped xs3p-in-panel-table">
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Super-types:</td>
<td><span class="type"><a href="#type_baseType" title="Jump to &quot;baseType&quot; type definition.">baseType</a></span> &lt; <strong>loopBase</strong> (by extension)</td>
</tr>
<tr class="even">
<td>Sub-types:</td>
<td><ul class="incremental">
<li><span class="type"><a href="#type_loopStandard" title="Jump to &quot;loopStandard&quot; type definition.">loopStandard</a></span> (by extension)</li>
<li><span class="type"><a href="#type_loopImpl" title="Jump to &quot;loopImpl&quot; type definition.">loopImpl</a></span> (by extension)</li>
</ul></td>
</tr>
</tbody>
</table>

#### <a href="#type_loopBase-properties-table-collapse" class="xs3p-panel-title">Properties</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

<table class="table table-striped xs3p-in-panel-table">
<tbody>
<tr class="odd">
<td>Name</td>
<td>loopBase</td>
</tr>
<tr class="even">
<td><a href="#term_Abstract" title="Look up &#39;Abstract&#39; in glossary">Abstract</a></td>
<td>yes</td>
</tr>
</tbody>
</table>

#### <a href="#type_loopBase-doc-panel-collapse" class="xs3p-panel-title">Documentation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

No documentation provided.

#### <a href="#type_loopBase-instance-table-collapse" class="xs3p-panel-title">XML Instance Representation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

    <...
     title="string" [0..1]
     minOccurs="nonNegativeInteger" [0..1]×Attribute minOccurs
                  The minimum number of times a loop may repeat. A value of 0 (zero)
                  indicates that the loop is optional.

                  When used in a loop defined
                  within an implementation,
                  the value may not be less than the value set on the standard loop referenced
                  by the implementation loop's 'type'
                  attribute.
                 Close  
     maxOccurs="nonNegativeInteger" [0..1]×Attribute maxOccurs
                  The maximum number of times a loop may repeat.
                  When used in a loop defined within an implementation, the value
                  may not be greater than
                  the value set on the standard loop referenced
                  by the implementation loop's 'type' attribute.
                 Close  
    >
       <tns:description> ... </tns:description> [0..1]
    </...>

#### <a href="#type_loopBase-schemaComponent-collapse" class="xs3p-panel-title collapsed">Schema Component Representation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

    <complexType name="loopBase" abstract="true">
       <complexContent>
          <extension base="tns:baseType">
             <attribute name="minOccurs" type="nonNegativeInteger" default="0"/>
             <attribute name="maxOccurs" type="nonNegativeInteger" default="1"/>
          </extension>
       </complexContent>
    </complexType>

[<span class="glyphicon glyphicon-chevron-up">
</span>](#top "Go to top of page")

------------------------------------------------------------------------

### Complex Type: <span id="type_loopImpl" class="name">loopImpl</span>

#### <a href="#type_loopImpl-type-hierarchy-collapse" class="xs3p-panel-title">Type hierarchy</a>

<table class="table table-striped xs3p-in-panel-table">
<tbody>
<tr class="odd">
<td>Super-types:</td>
<td><span class="type"><a href="#type_baseType" title="Jump to &quot;baseType&quot; type definition.">baseType</a></span> &lt; <span class="type"><a href="#type_loopBase" title="Jump to &quot;loopBase&quot; type definition.">loopBase</a></span> (by extension) &lt; <strong>loopImpl</strong> (by extension)</td>
</tr>
<tr class="even">
<td>Sub-types:</td>
<td>None</td>
</tr>
</tbody>
</table>

#### <a href="#type_loopImpl-properties-table-collapse" class="xs3p-panel-title">Properties</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

<table class="table table-striped xs3p-in-panel-table">
<tbody>
<tr class="odd">
<td>Name</td>
<td>loopImpl</td>
</tr>
<tr class="even">
<td><a href="#term_Abstract" title="Look up &#39;Abstract&#39; in glossary">Abstract</a></td>
<td>no</td>
</tr>
</tbody>
</table>

#### <a href="#type_loopImpl-doc-panel-collapse" class="xs3p-panel-title">Documentation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

No documentation provided.

#### <a href="#type_loopImpl-instance-table-collapse" class="xs3p-panel-title">XML Instance Representation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

    <...
     title="string" [0..1]
     minOccurs="nonNegativeInteger" [0..1]×Attribute minOccurs
                  The minimum number of times a loop may repeat. A value of 0 (zero)
                  indicates that the loop is optional.

                  When used in a loop defined
                  within an implementation,
                  the value may not be less than the value set on the standard loop referenced
                  by the implementation loop's 'type'
                  attribute.
                 Close  
     maxOccurs="nonNegativeInteger" [0..1]×Attribute maxOccurs
                  The maximum number of times a loop may repeat.
                  When used in a loop defined within an implementation, the value
                  may not be greater than
                  the value set on the standard loop referenced
                  by the implementation loop's 'type' attribute.
                 Close  
     type="NMTOKEN" [1]×Attribute type
                  The identifier (code attribute) of the standard loop this loop
                  implements.
                 Close  
     code="NMTOKEN" [1]×Attribute code
                  Code used to uniquely identify a loop implementation within the
                  transaction/message implementation.
                 Close  
     discriminator="tns:discriminatorType" [0..1]×Attribute discriminator
                  The element position in the loop's first segment used to identify an
                  implementation of a standard loop from other implementations. The
                  element identified by the position given in this attribute must also specify an
                  enumeration of values used only by this implementation and not used
                  by any other implementations of the standard loop at the same level of the
                  transaction.
                 Close  
    >
       <tns:description> ... </tns:description> [0..1]
       <tns:sequence   > [1]   
          Start Choice [1..*]
             <tns:segment> tns:segmentImpl </tns:segment> [1]
             <tns:loop> tns:loopImpl </tns:loop> [0..1]
          End Choice
       </tns:sequence>
    </...>

#### <a href="#type_loopImpl-schemaComponent-collapse" class="xs3p-panel-title collapsed">Schema Component Representation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

    <complexType name="loopImpl">
       <complexContent>
          <extension base="tns:loopBase">
             <sequence>
                <element name="sequence">
                   <complexType>
                      <choice maxOccurs="unbounded">
                         <element name="segment" type="tns:segmentImpl"/>
                         <element name="loop" type="tns:loopImpl" minOccurs="0"/>
                      </choice>
                   </complexType>
                </element>
             </sequence>
             <attribute name="type" type="NMTOKEN" use="required"/>
             <attribute name="code" type="NMTOKEN" use="required"/>
             <attribute name="discriminator" type="tns:discriminatorType"/>
          </extension>
       </complexContent>
    </complexType>

[<span class="glyphicon glyphicon-chevron-up">
</span>](#top "Go to top of page")

------------------------------------------------------------------------

### Complex Type: <span id="type_loopStandard" class="name">loopStandard</span>

#### <a href="#type_loopStandard-type-hierarchy-collapse" class="xs3p-panel-title">Type hierarchy</a>

<table class="table table-striped xs3p-in-panel-table">
<tbody>
<tr class="odd">
<td>Super-types:</td>
<td><span class="type"><a href="#type_baseType" title="Jump to &quot;baseType&quot; type definition.">baseType</a></span> &lt; <span class="type"><a href="#type_loopBase" title="Jump to &quot;loopBase&quot; type definition.">loopBase</a></span> (by extension) &lt; <strong>loopStandard</strong> (by extension)</td>
</tr>
<tr class="even">
<td>Sub-types:</td>
<td>None</td>
</tr>
</tbody>
</table>

#### <a href="#type_loopStandard-properties-table-collapse" class="xs3p-panel-title">Properties</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

<table class="table table-striped xs3p-in-panel-table">
<tbody>
<tr class="odd">
<td>Name</td>
<td>loopStandard</td>
</tr>
<tr class="even">
<td><a href="#term_Abstract" title="Look up &#39;Abstract&#39; in glossary">Abstract</a></td>
<td>no</td>
</tr>
</tbody>
</table>

#### <a href="#type_loopStandard-doc-panel-collapse" class="xs3p-panel-title">Documentation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

No documentation provided.

#### <a href="#type_loopStandard-instance-table-collapse" class="xs3p-panel-title">XML Instance Representation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

    <...
     title="string" [0..1]
     minOccurs="nonNegativeInteger" [0..1]×Attribute minOccurs
                  The minimum number of times a loop may repeat. A value of 0 (zero)
                  indicates that the loop is optional.

                  When used in a loop defined
                  within an implementation,
                  the value may not be less than the value set on the standard loop referenced
                  by the implementation loop's 'type'
                  attribute.
                 Close  
     maxOccurs="nonNegativeInteger" [0..1]×Attribute maxOccurs
                  The maximum number of times a loop may repeat.
                  When used in a loop defined within an implementation, the value
                  may not be greater than
                  the value set on the standard loop referenced
                  by the implementation loop's 'type' attribute.
                 Close  
     code="NMTOKEN" [1]×Attribute code
                  Code used to uniquely identify a loop within the transaction/message.
                 Close  
    >
       <tns:description> ... </tns:description> [0..1]
       <tns:sequence   > [1]   
          Start Choice [1..*]
             <tns:segment> tns:segmentStandard </tns:segment> [1]
             <tns:loop> tns:loopStandard </tns:loop> [0..1]
          End Choice
       </tns:sequence>
       <tns:syntax> ... </tns:syntax> [0..*]
    </...>

#### <a href="#type_loopStandard-schemaComponent-collapse" class="xs3p-panel-title collapsed">Schema Component Representation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

    <complexType name="loopStandard">
       <complexContent>
          <extension base="tns:loopBase">
             <sequence>
                <element name="sequence">
                   <complexType>
                      <choice maxOccurs="unbounded">
                         <element name="segment" type="tns:segmentStandard"/>
                         <element name="loop" type="tns:loopStandard" minOccurs="0"/>
                      </choice>
                   </complexType>
                </element>
                <element ref="tns:syntax" minOccurs="0" maxOccurs="unbounded"/>
             </sequence>
             <attribute name="code" type="NMTOKEN" use="required"/>
          </extension>
       </complexContent>
    </complexType>

[<span class="glyphicon glyphicon-chevron-up">
</span>](#top "Go to top of page")

------------------------------------------------------------------------

### Complex Type: <span id="type_segmentImpl" class="name">segmentImpl</span>

#### <a href="#type_segmentImpl-type-hierarchy-collapse" class="xs3p-panel-title">Type hierarchy</a>

<table class="table table-striped xs3p-in-panel-table">
<tbody>
<tr class="odd">
<td>Super-types:</td>
<td><span class="type"><a href="#type_baseType" title="Jump to &quot;baseType&quot; type definition.">baseType</a></span> &lt; <strong>segmentImpl</strong> (by extension)</td>
</tr>
<tr class="even">
<td>Sub-types:</td>
<td>None</td>
</tr>
</tbody>
</table>

#### <a href="#type_segmentImpl-properties-table-collapse" class="xs3p-panel-title">Properties</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

<table class="table table-striped xs3p-in-panel-table">
<tbody>
<tr class="odd">
<td>Name</td>
<td>segmentImpl</td>
</tr>
<tr class="even">
<td><a href="#term_Abstract" title="Look up &#39;Abstract&#39; in glossary">Abstract</a></td>
<td>no</td>
</tr>
</tbody>
</table>

#### <a href="#type_segmentImpl-doc-panel-collapse" class="xs3p-panel-title">Documentation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

No documentation provided.

#### <a href="#type_segmentImpl-instance-table-collapse" class="xs3p-panel-title">XML Instance Representation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

    <...
     title="string" [0..1]
     type="NCName" [1]×Attribute type
                  The name of the standard segment used at this position in the implementation.
                  Must be a valid segment name that occurs in the same
                  standard loop.
                 Close  
     code="NMTOKEN" [0..1]×Attribute code
                  Code used to identify a segment within a loop. May be useful when occurrences of a
                  standard segment contain distinct information.
                 Close  
     minOccurs="nonNegativeInteger" [0..1]×Attribute minOccurs
              The minimum number of times a type may occur at the declared location
              in the EDI structure.
             Close  
     maxOccurs="nonNegativeInteger" [0..1]×Attribute maxOccurs
              The maximum number of times a type may occur at the declared location
              in the EDI structure.
             Close  
     discriminator="tns:discriminatorType" [0..1]×Attribute discriminator
                  The element position in the segment used to identify an occurrence
                  of a standard segment from other implementation occurrences. The
                  element identified by the position given in this attribute must also specify an
                  enumeration of values used only by this implementation and not used
                  by any other implementations of the standard segment in the same implementation loop.
                 Close  
    >
       <tns:description> ... </tns:description> [0..1]
       <tns:sequence   > [0..1]   
          Start Choice [0..*]
             <tns:element> tns:elementImpl </tns:element> [1]
             <tns:composite> tns:compositeImpl </tns:composite> [1]
          End Choice
       </tns:sequence>
    </...>

#### <a href="#type_segmentImpl-schemaComponent-collapse" class="xs3p-panel-title collapsed">Schema Component Representation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

    <complexType name="segmentImpl">
       <complexContent>
          <extension base="tns:baseType">
             <sequence>
                <element name="sequence" minOccurs="0">
                   <complexType>
                      <sequence>
                         <choice minOccurs="0" maxOccurs="unbounded">
                            <element name="element" type="tns:elementImpl"/>
                            <element name="composite" type="tns:compositeImpl"/>
                         </choice>
                      </sequence>
                   </complexType>
                </element>
             </sequence>
             <attribute name="type" type="NCName" use="required"/>
             <attribute name="code" type="NMTOKEN" use="optional"/>
             <attributeGroup ref="tns:implementationAttributeGroup"/>
             <attribute name="discriminator" type="tns:discriminatorType" use="optional"/>
          </extension>
       </complexContent>
    </complexType>

[<span class="glyphicon glyphicon-chevron-up">
</span>](#top "Go to top of page")

------------------------------------------------------------------------

### Complex Type: <span id="type_segmentStandard" class="name">segmentStandard</span>

#### <a href="#type_segmentStandard-type-hierarchy-collapse" class="xs3p-panel-title">Type hierarchy</a>

<table class="table table-striped xs3p-in-panel-table">
<tbody>
<tr class="odd">
<td>Super-types:</td>
<td><span class="type"><a href="#type_baseType" title="Jump to &quot;baseType&quot; type definition.">baseType</a></span> &lt; <strong>segmentStandard</strong> (by extension)</td>
</tr>
<tr class="even">
<td>Sub-types:</td>
<td>None</td>
</tr>
</tbody>
</table>

#### <a href="#type_segmentStandard-properties-table-collapse" class="xs3p-panel-title">Properties</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

<table class="table table-striped xs3p-in-panel-table">
<tbody>
<tr class="odd">
<td>Name</td>
<td>segmentStandard</td>
</tr>
<tr class="even">
<td><a href="#term_Abstract" title="Look up &#39;Abstract&#39; in glossary">Abstract</a></td>
<td>no</td>
</tr>
</tbody>
</table>

#### <a href="#type_segmentStandard-doc-panel-collapse" class="xs3p-panel-title">Documentation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

No documentation provided.

#### <a href="#type_segmentStandard-instance-table-collapse" class="xs3p-panel-title">XML Instance Representation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

    <...
     title="string" [0..1]
     type="NCName" [0..1]×Attribute type
              The name of the target type being referenced.
             Close  
     minOccurs="nonNegativeInteger" [0..1]×Attribute minOccurs
              The minimum number of times a type may occur at the declared location
              in the EDI structure.
             Close  
     maxOccurs="nonNegativeInteger" [0..1]×Attribute maxOccurs
              The maximum number of times a type may occur at the declared location
              in the EDI structure.
             Close  
    >
       <tns:description> ... </tns:description> [0..1]
    </...>

#### <a href="#type_segmentStandard-schemaComponent-collapse" class="xs3p-panel-title collapsed">Schema Component Representation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

    <complexType name="segmentStandard">
       <complexContent>
          <extension base="tns:baseType">
             <attributeGroup ref="tns:referenceAttributeGroup"/>
          </extension>
       </complexContent>
    </complexType>

[<span class="glyphicon glyphicon-chevron-up">
</span>](#top "Go to top of page")

------------------------------------------------------------------------

### Complex Type: <span id="type_transactionControlType" class="name">transactionControlType</span>

#### <a href="#type_transactionControlType-type-hierarchy-collapse" class="xs3p-panel-title">Type hierarchy</a>

<table class="table table-striped xs3p-in-panel-table">
<tbody>
<tr class="odd">
<td>Super-types:</td>
<td><span class="type"><a href="#type_baseType" title="Jump to &quot;baseType&quot; type definition.">baseType</a></span> &lt; <span class="type"><a href="#type_controlType" title="Jump to &quot;controlType&quot; type definition.">controlType</a></span> (by extension) &lt; <strong>transactionControlType</strong> (by extension)</td>
</tr>
<tr class="even">
<td>Sub-types:</td>
<td>None</td>
</tr>
</tbody>
</table>

#### <a href="#type_transactionControlType-properties-table-collapse" class="xs3p-panel-title">Properties</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

<table class="table table-striped xs3p-in-panel-table">
<tbody>
<tr class="odd">
<td>Name</td>
<td>transactionControlType</td>
</tr>
<tr class="even">
<td><a href="#term_Abstract" title="Look up &#39;Abstract&#39; in glossary">Abstract</a></td>
<td>no</td>
</tr>
</tbody>
</table>

#### <a href="#type_transactionControlType-doc-panel-collapse" class="xs3p-panel-title">Documentation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

No documentation provided.

#### <a href="#type_transactionControlType-instance-table-collapse" class="xs3p-panel-title">XML Instance Representation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

    <...
     title="string" [0..1]
     header="NCName" [1]
     trailer="NCName" [1]
     use="tns:useType" [0..1]
    >
       <tns:description> ... </tns:description> [0..1]
    </...>

#### <a href="#type_transactionControlType-schemaComponent-collapse" class="xs3p-panel-title collapsed">Schema Component Representation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

    <complexType name="transactionControlType">
       <complexContent>
          <extension base="tns:controlType">
             <attribute name="use" type="tns:useType" default="optional"/>
          </extension>
       </complexContent>
    </complexType>

[<span class="glyphicon glyphicon-chevron-up">
</span>](#top "Go to top of page")

------------------------------------------------------------------------

### Simple Type: <span id="type_discriminatorType" class="name">discriminatorType</span>

#### <a href="#type_discriminatorType-type-hierarchy-collapse" class="xs3p-panel-title">Type hierarchy</a>

<table class="table table-striped xs3p-in-panel-table">
<tbody>
<tr class="odd">
<td>Super-types:</td>
<td><span class="type">decimal</span> &lt; <strong>discriminatorType</strong> (by restriction)</td>
</tr>
<tr class="even">
<td>Sub-types:</td>
<td>None</td>
</tr>
</tbody>
</table>

#### <a href="#type_discriminatorType-properties-table-collapse" class="xs3p-panel-title">Properties</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

<table class="table table-striped xs3p-in-panel-table">
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Name</td>
<td>discriminatorType</td>
</tr>
<tr class="even">
<td>Content</td>
<td><ul class="incremental">
<li>Base XSD Type: decimal</li>
</ul>
<ul class="incremental">
<li><em>pattern</em> = [0-9]+(\.[0-9]{1,2}){0,1}</li>
<li>1 &lt;= <em>value</em> &lt;= 99.99</li>
</ul></td>
</tr>
</tbody>
</table>

#### <a href="#type_discriminatorType-doc-panel-collapse" class="xs3p-panel-title">Documentation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

No documentation provided.

#### <a href="#type_discriminatorType-schemaComponent-collapse" class="xs3p-panel-title collapsed">Schema Component Representation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

    <simpleType name="discriminatorType">
       <restriction base="decimal">
          <minInclusive value="1"/>
          <maxInclusive value="99.99"/>
          <pattern value="[0-9]+(\.[0-9]{1,2}){0,1}"/>
       </restriction>
    </simpleType>

[<span class="glyphicon glyphicon-chevron-up">
</span>](#top "Go to top of page")

------------------------------------------------------------------------

### Simple Type: <span id="type_elementBaseType" class="name">elementBaseType</span>

#### <a href="#type_elementBaseType-type-hierarchy-collapse" class="xs3p-panel-title">Type hierarchy</a>

<table class="table table-striped xs3p-in-panel-table">
<tbody>
<tr class="odd">
<td>Super-types:</td>
<td><span class="type">string</span> &lt; <strong>elementBaseType</strong> (by restriction)</td>
</tr>
<tr class="even">
<td>Sub-types:</td>
<td>None</td>
</tr>
</tbody>
</table>

#### <a href="#type_elementBaseType-properties-table-collapse" class="xs3p-panel-title">Properties</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

<table class="table table-striped xs3p-in-panel-table">
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Name</td>
<td>elementBaseType</td>
</tr>
<tr class="even">
<td>Content</td>
<td><ul class="incremental">
<li>Base XSD Type: string</li>
</ul>
<ul class="incremental">
<li><em>value</em> comes from list: { 'binary'| 'date'| 'decimal'| 'identifier'| 'numeric'| 'string'| 'time'}</li>
</ul></td>
</tr>
</tbody>
</table>

#### <a href="#type_elementBaseType-doc-panel-collapse" class="xs3p-panel-title">Documentation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

No documentation provided.

#### <a href="#type_elementBaseType-schemaComponent-collapse" class="xs3p-panel-title collapsed">Schema Component Representation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

    <simpleType name="elementBaseType">
       <restriction base="string">
          <enumeration value="binary"/>
          <enumeration value="date"/>
          <enumeration value="decimal"/>
          <enumeration value="identifier"/>
          <enumeration value="numeric"/>
          <enumeration value="string"/>
          <enumeration value="time"/>
       </restriction>
    </simpleType>

[<span class="glyphicon glyphicon-chevron-up">
</span>](#top "Go to top of page")

------------------------------------------------------------------------

### Simple Type: <span id="type_nameType" class="name">nameType</span>

#### <a href="#type_nameType-type-hierarchy-collapse" class="xs3p-panel-title">Type hierarchy</a>

<table class="table table-striped xs3p-in-panel-table">
<tbody>
<tr class="odd">
<td>Super-types:</td>
<td><span class="type">ID</span> &lt; <strong>nameType</strong> (by restriction)</td>
</tr>
<tr class="even">
<td>Sub-types:</td>
<td>None</td>
</tr>
</tbody>
</table>

#### <a href="#type_nameType-properties-table-collapse" class="xs3p-panel-title">Properties</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

<table class="table table-striped xs3p-in-panel-table">
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Name</td>
<td>nameType</td>
</tr>
<tr class="even">
<td>Content</td>
<td><ul class="incremental">
<li>Base XSD Type: ID</li>
</ul>
<ul class="incremental">
<li><em>pattern</em> = [A-Z][A-Z0-9]+</li>
</ul></td>
</tr>
</tbody>
</table>

#### <a href="#type_nameType-doc-panel-collapse" class="xs3p-panel-title">Documentation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

No documentation provided.

#### <a href="#type_nameType-schemaComponent-collapse" class="xs3p-panel-title collapsed">Schema Component Representation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

    <simpleType name="nameType">
       <restriction base="ID">
          <pattern value="[A-Z][A-Z0-9]+"/>
       </restriction>
    </simpleType>

[<span class="glyphicon glyphicon-chevron-up">
</span>](#top "Go to top of page")

------------------------------------------------------------------------

### Simple Type: <span id="type_positionType" class="name">positionType</span>

#### <a href="#type_positionType-type-hierarchy-collapse" class="xs3p-panel-title">Type hierarchy</a>

<table class="table table-striped xs3p-in-panel-table">
<tbody>
<tr class="odd">
<td>Super-types:</td>
<td><span class="type">nonNegativeInteger</span> &lt; <strong>positionType</strong> (by restriction)</td>
</tr>
<tr class="even">
<td>Sub-types:</td>
<td>None</td>
</tr>
</tbody>
</table>

#### <a href="#type_positionType-properties-table-collapse" class="xs3p-panel-title">Properties</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

<table class="table table-striped xs3p-in-panel-table">
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Name</td>
<td>positionType</td>
</tr>
<tr class="even">
<td>Content</td>
<td><ul class="incremental">
<li>Base XSD Type: nonNegativeInteger</li>
</ul>
<ul class="incremental">
<li><em>value</em> &gt;= 1</li>
</ul></td>
</tr>
</tbody>
</table>

#### <a href="#type_positionType-doc-panel-collapse" class="xs3p-panel-title">Documentation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

No documentation provided.

#### <a href="#type_positionType-schemaComponent-collapse" class="xs3p-panel-title collapsed">Schema Component Representation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

    <simpleType name="positionType">
       <restriction base="nonNegativeInteger">
          <minInclusive value="1"/>
       </restriction>
    </simpleType>

[<span class="glyphicon glyphicon-chevron-up">
</span>](#top "Go to top of page")

------------------------------------------------------------------------

### Simple Type: <span id="type_syntaxType" class="name">syntaxType</span>

#### <a href="#type_syntaxType-type-hierarchy-collapse" class="xs3p-panel-title">Type hierarchy</a>

<table class="table table-striped xs3p-in-panel-table">
<tbody>
<tr class="odd">
<td>Super-types:</td>
<td><span class="type">string</span> &lt; <strong>syntaxType</strong> (by restriction)</td>
</tr>
<tr class="even">
<td>Sub-types:</td>
<td>None</td>
</tr>
</tbody>
</table>

#### <a href="#type_syntaxType-properties-table-collapse" class="xs3p-panel-title">Properties</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

<table class="table table-striped xs3p-in-panel-table">
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Name</td>
<td>syntaxType</td>
</tr>
<tr class="even">
<td>Content</td>
<td><ul class="incremental">
<li>Base XSD Type: string</li>
</ul>
<ul class="incremental">
<li><em>value</em> comes from list: { 'single'| 'paired'| 'required'| 'exclusion'| 'conditional'| 'list'| 'firstonly'}</li>
</ul></td>
</tr>
</tbody>
</table>

#### <a href="#type_syntaxType-doc-panel-collapse" class="xs3p-panel-title">Documentation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

No documentation provided.

#### <a href="#type_syntaxType-schemaComponent-collapse" class="xs3p-panel-title collapsed">Schema Component Representation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

    <simpleType name="syntaxType">
       <restriction base="string">
          <enumeration value="single"/>
          <enumeration value="paired"/>
          <enumeration value="required"/>
          <enumeration value="exclusion"/>
          <enumeration value="conditional"/>
          <enumeration value="list"/>
          <enumeration value="firstonly"/>
       </restriction>
    </simpleType>

[<span class="glyphicon glyphicon-chevron-up">
</span>](#top "Go to top of page")

------------------------------------------------------------------------

### Simple Type: <span id="type_useType" class="name">useType</span>

#### <a href="#type_useType-type-hierarchy-collapse" class="xs3p-panel-title">Type hierarchy</a>

<table class="table table-striped xs3p-in-panel-table">
<tbody>
<tr class="odd">
<td>Super-types:</td>
<td><span class="type">string</span> &lt; <strong>useType</strong> (by restriction)</td>
</tr>
<tr class="even">
<td>Sub-types:</td>
<td>None</td>
</tr>
</tbody>
</table>

#### <a href="#type_useType-properties-table-collapse" class="xs3p-panel-title">Properties</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

<table class="table table-striped xs3p-in-panel-table">
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Name</td>
<td>useType</td>
</tr>
<tr class="even">
<td>Content</td>
<td><ul class="incremental">
<li>Base XSD Type: string</li>
</ul>
<ul class="incremental">
<li><em>value</em> comes from list: {'required'|'optional'|'prohibited'}</li>
</ul></td>
</tr>
</tbody>
</table>

#### <a href="#type_useType-doc-panel-collapse" class="xs3p-panel-title">Documentation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

No documentation provided.

#### <a href="#type_useType-schemaComponent-collapse" class="xs3p-panel-title collapsed">Schema Component Representation</a><span class="pull-right xs3p-panel-help"> <span class="glyphicon glyphicon-question-sign"> </span></span>

    <simpleType name="useType">
       <restriction base="string">
          <enumeration value="required"/>
          <enumeration value="optional"/>
          <enumeration value="prohibited"/>
       </restriction>
    </simpleType>

[<span class="glyphicon glyphicon-chevron-up">
</span>](#top "Go to top of page")

------------------------------------------------------------------------

<span id="Glossary">Glossary</span>
-----------------------------------

<span class="glossaryTerm"><span id="term_Abstract">Abstract</span>
</span>(Applies to complex type definitions and element declarations).
An abstract element or complex type cannot used to validate an element
instance. If there is a reference to an abstract element, only element
declarations that can substitute the abstract element can be used to
validate the instance. For references to abstract type definitions, only
derived types can be used.

<span class="glossaryTerm"><span id="term_All">All Model Group</span>
</span>Child elements can be provided *in any order* in instances. See:
<http://www.w3.org/TR/xmlschema-1/#element-all>.

<span class="glossaryTerm"><span id="term_Choice">Choice Model
Group</span> </span>*Only one* from the list of child elements and model
groups can be provided in instances. See:
<http://www.w3.org/TR/xmlschema-1/#element-choice>.

<span class="glossaryTerm"><span id="term_CollapseWS">Collapse
Whitespace Policy</span> </span>Replace tab, line feed, and carriage
return characters with space character (Unicode character 32). Then,
collapse contiguous sequences of space characters into single space
character, and remove leading and trailing space characters.

<span class="glossaryTerm"><span id="term_ElemBlock">Disallowed
Substitutions</span> </span>(Applies to element declarations). If
*substitution* is specified, then [substitution
group](#term_SubGroup "Look up 'substitution group' in glossary")
members cannot be used in place of the given element declaration to
validate element instances. If *derivation methods*, e.g. extension,
restriction, are specified, then the given element declaration will not
validate element instances that have types derived from the element
declaration's type using the specified derivation methods. Normally,
element instances can override their declaration's type by specifying an
`xsi:type` attribute.

<span class="glossaryTerm"><span id="term_Key">Key Constraint</span>
</span>Like [Uniqueness
Constraint](#term_Unique "Look up 'Uniqueness Constraint' in glossary"),
but additionally requires that the specified value(s) must be provided.
See:
<http://www.w3.org/TR/xmlschema-1/#cIdentity-constraint_Definitions>.

<span class="glossaryTerm"><span id="term_KeyRef">Key Reference
Constraint</span> </span>Ensures that the specified value(s) must match
value(s) from a [Key
Constraint](#term_Key "Look up 'Key Constraint' in glossary") or
[Uniqueness
Constraint](#term_Unique "Look up 'Uniqueness Constraint' in glossary").
See:
<http://www.w3.org/TR/xmlschema-1/#cIdentity-constraint_Definitions>.

<span class="glossaryTerm"><span id="term_ModelGroup">Model Group</span>
</span>Groups together element content, specifying the order in which
the element content can occur and the number of times the group of
element content may be repeated. See:
<http://www.w3.org/TR/xmlschema-1/#Model_Groups>.

<span class="glossaryTerm"><span id="term_Nillable">Nillable</span>
</span>(Applies to element declarations). If an element declaration is
nillable, instances can use the `xsi:nil` attribute. The `xsi:nil`
attribute is the boolean attribute, *nil*, from the
*http://www.w3.org/2001/XMLSchema-instance* namespace. If an element
instance has an `xsi:nil` attribute set to true, it can be left empty,
even though its element declaration may have required content.

<span class="glossaryTerm"><span id="term_Notation">Notation</span>
</span>A notation is used to identify the format of a piece of data.
Values of elements and attributes that are of type, NOTATION, must come
from the names of declared notations. See:
<http://www.w3.org/TR/xmlschema-1/#cNotation_Declarations>.

<span class="glossaryTerm"><span id="term_PreserveWS">Preserve
Whitespace Policy</span> </span>Preserve whitespaces exactly as they
appear in instances.

<span class="glossaryTerm"><span id="term_TypeFinal">Prohibited
Derivations</span> </span>(Applies to type definitions). Derivation
methods that cannot be used to create sub-types from a given type
definition.

<span class="glossaryTerm"><span id="term_TypeBlock">Prohibited
Substitutions</span> </span>(Applies to complex type definitions).
Prevents sub-types that have been derived using the specified derivation
methods from validating element instances in place of the given type
definition.

<span class="glossaryTerm"><span id="term_ReplaceWS">Replace Whitespace
Policy</span> </span>Replace tab, line feed, and carriage return
characters with space character (Unicode character 32).

<span class="glossaryTerm"><span id="term_Sequence">Sequence Model
Group</span> </span>Child elements and model groups must be provided *in
the specified order* in instances. See:
<http://www.w3.org/TR/xmlschema-1/#element-sequence>.

<span class="glossaryTerm"><span id="term_SubGroup">Substitution
Group</span> </span>Elements that are *members* of a substitution group
can be used wherever the *head* element of the substitution group is
referenced.

<span class="glossaryTerm"><span id="term_ElemFinal">Substitution Group
Exclusions</span> </span>(Applies to element declarations). Prohibits
element declarations from nominating themselves as being able to
substitute a given element declaration, if they have types that are
derived from the original element's type using the specified derivation
methods.

<span class="glossaryTerm"><span id="term_TargetNS">Target
Namespace</span> </span>The target namespace identifies the namespace
that components in this schema belongs to. If no target namespace is
provided, then the schema components do not belong to any namespace.

<span class="glossaryTerm"><span id="term_Unique">Uniqueness
Constraint</span> </span>Ensures uniqueness of an element/attribute
value, or a combination of values, within a specified scope. See:
<http://www.w3.org/TR/xmlschema-1/#cIdentity-constraint_Definitions>.

[<span class="glyphicon glyphicon-chevron-up">
</span>](#top "Go to top of page")

------------------------------------------------------------------------

Generated by [xs3p](https://github.com/Mapudo/xs3p).
