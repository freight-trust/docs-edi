 EDI Schema Documentation    /\* prettier-ignore-start \*/ /\* XS3P specific CSS \*/ body { background-color: #fff; padding-top: 50px; } .nav > li.active { background-color: #fff; } .nav > li > a:hover { background-color: #ccc; } code { color: #333; } .container-fluid { padding: 15px 15px; } .nav-sub-item > a { padding-left: 30px !important; } a.name { padding-top: 65px; } h3.xs3p-subsection-heading { margin-bottom: 30px; } section, #top { margin-top: -65px; padding-top: 65px; } pre { padding: 5px; } .xs3p-sidenav { padding-top: 10px; padding-bottom: 10px; background-color: #eee; border-radius: 10px; } .xs3p-navbar-title { color: #fff !important; font-weight: bold; } .xs3p-in-panel-table { margin-bottom: 0px; } .xs3p-sidebar { position: static; } .xs3p-collapse-button { font-size: 8pt; } .panel-heading .xs3p-panel-title:after { font-family: "Glyphicons Halflings"; content: "\\e114"; float: left; color: grey; margin-right: 10px; } .panel-heading .xs3p-panel-title.collapsed:after { content: "\\e080"; } .panel-info > .panel-heading .xs3p-panel-title:after { color: white; } .xs3p-panel-help { color: #cccccc; cursor: pointer; } .panel-group { margin-bottom: 20px; } .btn-doc { padding: 0px; border: 0px none; background: none repeat scroll 0% 0% transparent; line-height: 1; font-size: 12px; } .unpre { font-family: "Helvetica Neue", Helvetica, Arial, sans-serif; font-size: 14px; white-space: normal; word-break: normal; word-wrap: normal; } .popover { max-width: 400px; } /\* <!-- Syntax highlighting --> \*/ .codehilite .err { color: #fff; background-color: #d2322d; font-weight: bold; } /\* Error \*/ .codehilite .c { color: #999; } .codehilite .cs { color: #999; font-style: italic; } .codehilite .nt { color: #2f6f9f; } .codehilite .nn { color: #39b3d7; } .codehilite .na { color: #47a447; } .codehilite .s { color: #d2322d; } .codehilite a { color: inherit !important; text-decoration: underline !important; } .codehilite a:hover { opacity: 0.7 !important; } @media (min-width: 992px) { .xs3p-sidebar { position: fixed; top: 65px; width: 22%; } } /\* prettier-ignore-end \*/   

Toggle navigation EDI Schema Documentation

*   [Schema Document Properties](#SchemaProperties)
*   [Global Declarations](#SchemaDeclarations)
*   [Element: **compositeType**](#element_compositeType)
*   [Element: **description**](#element_description)
*   [Element: **elementType**](#element_elementType)
*   [Element: **enumeration**](#element_enumeration)
*   [Element: **implementation**](#element_implementation)
*   [Element: **include**](#element_include)
*   [Element: **interchange**](#element_interchange)
*   [Element: **schema**](#element_schema)
*   [Element: **segmentType**](#element_segmentType)
*   [Element: **syntax**](#element_syntax)
*   [Element: **transaction**](#element_transaction)
*   [Global Definitions](#SchemaDefinitions)
*   [Attribute Group: **implementationAttributeGroup**](#attributeGroup_implementationAttributeGroup)
*   [Attribute Group: **lengthAttributeGroup**](#attributeGroup_lengthAttributeGroup)
*   [Attribute Group: **occursAttributeGroup**](#attributeGroup_occursAttributeGroup)
*   [Attribute Group: **referenceAttributeGroup**](#attributeGroup_referenceAttributeGroup)
*   [Attribute Group: **versionAttributeGroup**](#attributeGroup_versionAttributeGroup)
*   [Complex Type: **anyElementType**](#type_anyElementType)
*   [Complex Type: **baseType**](#type_baseType)
*   [Complex Type: **compositeImpl**](#type_compositeImpl)
*   [Complex Type: **compositeStandard**](#type_compositeStandard)
*   [Complex Type: **controlType**](#type_controlType)
*   [Complex Type: **elementImpl**](#type_elementImpl)
*   [Complex Type: **elementStandard**](#type_elementStandard)
*   [Complex Type: **groupControlType**](#type_groupControlType)
*   [Complex Type: **loopBase**](#type_loopBase)
*   [Complex Type: **loopImpl**](#type_loopImpl)
*   [Complex Type: **loopStandard**](#type_loopStandard)
*   [Complex Type: **segmentImpl**](#type_segmentImpl)
*   [Complex Type: **segmentStandard**](#type_segmentStandard)
*   [Complex Type: **transactionControlType**](#type_transactionControlType)
*   [Simple Type: **discriminatorType**](#type_discriminatorType)
*   [Simple Type: **elementBaseType**](#type_elementBaseType)
*   [Simple Type: **nameType**](#type_nameType)
*   [Simple Type: **positionType**](#type_positionType)
*   [Simple Type: **syntaxType**](#type_syntaxType)
*   [Simple Type: **useType**](#type_useType)
*   [Glossary](#Glossary)

×

#### Attribute minOccurs

The minimum number of times an undefined element may occur at the declared location in the EDI structure.

Close

×

#### Attribute maxOccurs

The maximum number of times an undefined element may occur at the declared location in the EDI structure.

Close

×

#### Attribute type

The name of the target type being referenced.

Close

×

#### Attribute minLength

The minimum length allowed for an element value to be valid.

Close

×

#### Attribute maxLength

The maximum length allowed for an element value to be valid.

Close

×

#### Attribute minOccurs

The minimum number of times a type may occur at the declared location in the EDI structure.

Close

×

#### Attribute maxOccurs

The maximum number of times a type may occur at the declared location in the EDI structure.

Close

×

#### Attribute minVersion

The minimum transaction version this schema version applies to.

Close

×

#### Attribute maxVersion

The maximum transaction version this schema version applies to.

Close

×

#### Attribute minOccurs

The minimum number of times a type may occur at the declared location in the EDI structure.

Close

×

#### Attribute maxOccurs

The maximum number of times a type may occur at the declared location in the EDI structure.

Close

×

#### Element sequence

The ordered elements for a composite element implementation.

Close

×

#### Element sequence

The ordered elements and components for a segment implementation.

Close

×

#### Attribute type

The name of the standard segment used at this position in the implementation. Must be a valid segment name that occurs in the same standard loop.

Close

×

#### Attribute code

Code used to identify a segment within a loop. May be useful when occurrences of a standard segment contain distinct information.

Close

×

#### Attribute discriminator

The element position in the segment used to identify an occurrence of a standard segment from other implementation occurrences. The element identified by the position given in this attribute must also specify an enumeration of values used only by this implementation and not used by any other implementations of the standard segment in the same implementation loop.

Close

×

#### Attribute minOccurs

The minimum number of times a loop may repeat. A value of 0 (zero) indicates that the loop is optional. When used in a loop defined within an implementation, the value may not be less than the value set on the standard loop referenced by the implementation loop's 'type' attribute.

Close

×

#### Attribute maxOccurs

The maximum number of times a loop may repeat. When used in a loop defined within an implementation, the value may not be greater than the value set on the standard loop referenced by the implementation loop's 'type' attribute.

Close

×

#### Element sequence

The ordered list of segments and sub-loops contained in this loop.

Close

×

#### Attribute code

Code used to uniquely identify a loop within the transaction/message.

Close

×

#### Element sequence

The ordered list of segments and sub-loops contained in this loop.

Close

×

#### Attribute type

The identifier (code attribute) of the standard loop this loop implements.

Close

×

#### Attribute code

Code used to uniquely identify a loop implementation within the transaction/message implementation.

Close

×

#### Attribute discriminator

The element position in the loop's first segment used to identify an implementation of a standard loop from other implementations. The element identified by the position given in this attribute must also specify an enumeration of values used only by this implementation and not used by any other implementations of the standard loop at the same level of the transaction.

Close

×

#### Element include

Optional reference to another schema file to include.

Close

×

#### Element sequence

The ordered list of segments and sub-loops contained at the top-level of this transaction.

Close

×

#### Element sequence

The ordered list of segments and sub-loops contained at the top-level of a transaction implementation.

Close

×

#### Attribute name

Code used to uniquely identify an element definition to be referenced by compositeType and segmentType elements within this schema. This value will be returned by an EDIStreamReader's \`getReferenceCode\` method when no \`code\` attribute has been specified.

Close

×

#### Attribute code

Code used to identify an element externally. This value will be returned by an EDIStreamReader's \`getReferenceCode\` method.

Close

×

#### Attribute number

\*DEPRECATED\* Use the \`code\` attribute to provide an element reference number.

Close

×

#### Attribute base

Identifies the element data type

Close

×

#### Attribute scale

For numeric base types only, scale is the number of digits to the right of an implied decimal point. When not specified, the default value of zero is used (i.e. the data type is integer)

Close

×

#### Element sequence

The ordered elements and syntax restrictions for a composite element.

Close

×

#### Element any

May be used to declare that any component element may occur in this composite type up to the maximum number given by maxOccurs. The value of minOccurs defines the number of undefined component elements that MUST occur in the composite.

Close

×

#### Attribute name

Code used to uniquely identify a composite element definition to be referenced by segmentType elements within this schema. This value will be returned by an EDIStreamReader's \`getReferenceCode\` method.

Close

×

#### Element segmentType

Used to declare a segment

Close

×

#### Element sequence

The ordered elements, components, and syntax restrictions for a segment.

Close

×

#### Element element

Defines a reference to a standard element definition.

Close

×

#### Element any

May be used to declare that any element or composite may occur in this segment type up to the maximum number given by maxOccurs. The value of minOccurs defines the number of undefined elements that MUST occur in the segment at this position. Elements that repeat may occur up to 99 times and are not affected by the value of the maxOccurs attribute.

Close

×

#### Attribute name

Name of the segment. Also referred to as the segment's tag. This is the two or three character string used to identify a segment.

Close

EDI Schema Documentation
========================

Schema Document Properties
--------------------------

#### [Properties](#schema-properties-table-collapse)

[Target Namespace](#term_TargetNS "Look up 'Target Namespace' in glossary")

http://freighttrust.io/EDISchema/v4

Element and Attribute Namespaces

*   Global element and attribute declarations belong to this schema's target namespace.
*   By default, local element declarations belong to this schema's target namespace.
*   By default, local attribute declarations have no namespace.

#### [Documentation](#schema-doc-panel-collapse)

No documentation provided.

#### [Declared Namespaces](#schema-declared-namespaces-collapse)

Prefix

Namespace

Default namespace

http://www.w3.org/2001/XMLSchema

xml

http://www.w3.org/XML/1998/namespace

tns

http://freighttrust.io/EDISchema/v4

#### [Schema Component Representation](#schema-schemaComponent-collapse)

<schema targetNamespace="http://freighttrust.io/EDISchema/v4" elementFormDefault="qualified"\>
...
</schema>

[](#top "Go to top of page")

* * *

Global Declarations
-------------------

### Element: compositeType

#### [Properties](#element_compositeType-properties-table-collapse)

Name

compositeType

Type

Locally-defined complex type

[Nillable](#term_Nillable "Look up 'Nillable' in glossary")

no

[Abstract](#term_Abstract "Look up 'Abstract' in glossary")

no

#### [Documentation](#element_compositeType-doc-panel-collapse)

No documentation provided.

#### [XML Instance Representation](#element_compositeType-instance-table-collapse)

<[tns](#ns_tns "Find out namespace of 'tns' prefix"):compositeType
 title="string" \[0..1\]
 name="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[nameType](#type_nameType "Jump to "nameType" type definition.")" \[1\]

×

#### Attribute name

                Code used to uniquely identify a composite element definition to be referenced by
                segmentType elements within this schema. This
                value will be returned by an EDIStreamReader's \`getReferenceCode\` method.
              

Close

 
\>
   <[tns](#ns_tns "Find out namespace of 'tns' prefix"):[description](#element_description "Jump to "description" element declaration.")\> ... </[tns](#ns_tns "Find out namespace of 'tns' prefix"):[description](#element_description "Jump to "description" element declaration.")\> \[0..1\]
   <[tns](#ns_tns "Find out namespace of 'tns' prefix"):sequence   \> \[1\]  
      Start [Choice](#term_Choice "Look up 'Choice' in glossary") \[1..\*\]
         <[tns](#ns_tns "Find out namespace of 'tns' prefix"):element> [tns](#ns_tns "Find out namespace of 'tns' prefix"):[elementStandard](#type_elementStandard "Jump to "elementStandard" type definition.") </[tns](#ns_tns "Find out namespace of 'tns' prefix"):element> \[1..\*\]
         <[tns](#ns_tns "Find out namespace of 'tns' prefix"):any> [tns](#ns_tns "Find out namespace of 'tns' prefix"):[anyElementType](#type_anyElementType "Jump to "anyElementType" type definition.") </[tns](#ns_tns "Find out namespace of 'tns' prefix"):any> \[1\] 
      End Choice
   </[tns](#ns_tns "Find out namespace of 'tns' prefix"):sequence>
   <[tns](#ns_tns "Find out namespace of 'tns' prefix"):[syntax](#element_syntax "Jump to "syntax" element declaration.")\> ... </[tns](#ns_tns "Find out namespace of 'tns' prefix"):[syntax](#element_syntax "Jump to "syntax" element declaration.")\> \[0..\*\]
</[tns](#ns_tns "Find out namespace of 'tns' prefix"):compositeType>

#### [Schema Component Representation](#element_compositeType-schemaComponent-collapse)

<element name="compositeType"\>
   <complexType\>
      <complexContent\>
         <extension base="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[baseType](#type_baseType "Jump to "baseType" type definition.")"\>
            <sequence\>
               <element name="sequence"\>
                  <complexType\>
                     <choice minOccurs="1" maxOccurs="unbounded"\>
                        <element name="element" type="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[elementStandard](#type_elementStandard "Jump to "elementStandard" type definition.")" minOccurs="1" maxOccurs="unbounded"/>
                        <element name="any" type="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[anyElementType](#type_anyElementType "Jump to "anyElementType" type definition.")"/>
                     </choice>
                  </complexType>
               </element>
               <element ref="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[syntax](#element_syntax "Jump to "syntax" element declaration.")" minOccurs="0" maxOccurs="unbounded"/>
            </sequence>
            <attribute name="name" type="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[nameType](#type_nameType "Jump to "nameType" type definition.")" use="required"/>
         </extension>
      </complexContent>
   </complexType>
</element>

[](#top "Go to top of page")

* * *

### Element: description

#### [Properties](#element_description-properties-table-collapse)

Name

description

Type

string

[Nillable](#term_Nillable "Look up 'Nillable' in glossary")

no

[Abstract](#term_Abstract "Look up 'Abstract' in glossary")

no

#### [Documentation](#element_description-doc-panel-collapse)

No documentation provided.

#### [XML Instance Representation](#element_description-instance-table-collapse)

<[tns](#ns_tns "Find out namespace of 'tns' prefix"):description> string </[tns](#ns_tns "Find out namespace of 'tns' prefix"):description>

#### [Schema Component Representation](#element_description-schemaComponent-collapse)

<element name="description" type="string"/>

[](#top "Go to top of page")

* * *

### Element: elementType

#### [Properties](#element_elementType-properties-table-collapse)

Name

elementType

Type

Locally-defined complex type

[Nillable](#term_Nillable "Look up 'Nillable' in glossary")

no

[Abstract](#term_Abstract "Look up 'Abstract' in glossary")

no

#### [Documentation](#element_elementType-doc-panel-collapse)

No documentation provided.

#### [XML Instance Representation](#element_elementType-instance-table-collapse)

<[tns](#ns_tns "Find out namespace of 'tns' prefix"):elementType
 title="string" \[0..1\]
 name="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[nameType](#type_nameType "Jump to "nameType" type definition.")" \[1\]

×

#### Attribute name

                Code used to uniquely identify an element definition to be referenced by
                compositeType and segmentType elements within this schema.
                This value will be returned by an EDIStreamReader's \`getReferenceCode\` method
                when no \`code\` attribute has been specified.
              

Close

 
 code="NMTOKEN" \[0..1\]

×

#### Attribute code

                Code used to identify an element externally. This value will
                be returned by an EDIStreamReader's \`getReferenceCode\` method.
              

Close

 
 number="nonNegativeInteger (1 <= _value_ <= 9999)" \[0..1\]

×

#### Attribute number

\*DEPRECATED\* Use the \`code\` attribute to provide an element reference number.

Close

 
 base="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[elementBaseType](#type_elementBaseType "Jump to "elementBaseType" type definition.")" \[0..1\]

×

#### Attribute base

                Identifies the element data type
              

Close

 
 scale="nonNegativeInteger" \[0..1\]

×

#### Attribute scale

                For numeric base types only, scale is the number of digits to the right of an implied decimal point. When not specified, the
                default value of zero is used (i.e. the data type is integer)
              

Close

 
 minLength="nonNegativeInteger" \[0..1\]

×

#### Attribute minLength

          The minimum length allowed for an element value to be valid.
        

Close

 
 maxLength="nonNegativeInteger" \[0..1\]

×

#### Attribute maxLength

          The maximum length allowed for an element value to be valid.
        

Close

 
\>
   <[tns](#ns_tns "Find out namespace of 'tns' prefix"):[description](#element_description "Jump to "description" element declaration.")\> ... </[tns](#ns_tns "Find out namespace of 'tns' prefix"):[description](#element_description "Jump to "description" element declaration.")\> \[0..1\]
   <[tns](#ns_tns "Find out namespace of 'tns' prefix"):[enumeration](#element_enumeration "Jump to "enumeration" element declaration.")\> ... </[tns](#ns_tns "Find out namespace of 'tns' prefix"):[enumeration](#element_enumeration "Jump to "enumeration" element declaration.")\> \[0..1\]
   <[tns](#ns_tns "Find out namespace of 'tns' prefix"):version
    minVersion="token" \[0..1\]

×

#### Attribute minVersion

          The minimum transaction version this schema version applies to.
        

Close

 
    maxVersion="token" \[0..1\]

×

#### Attribute maxVersion

          The maximum transaction version this schema version applies to.
        

Close

 
    minLength="nonNegativeInteger" \[0..1\]

×

#### Attribute minLength

          The minimum length allowed for an element value to be valid.
        

Close

 
    maxLength="nonNegativeInteger" \[0..1\]

×

#### Attribute maxLength

          The maximum length allowed for an element value to be valid.
        

Close

 
   \> \[0..\*\] 
      <[tns](#ns_tns "Find out namespace of 'tns' prefix"):[enumeration](#element_enumeration "Jump to "enumeration" element declaration.")\> ... </[tns](#ns_tns "Find out namespace of 'tns' prefix"):[enumeration](#element_enumeration "Jump to "enumeration" element declaration.")\> \[0..1\]
   </[tns](#ns_tns "Find out namespace of 'tns' prefix"):version>
</[tns](#ns_tns "Find out namespace of 'tns' prefix"):elementType>

#### [Schema Component Representation](#element_elementType-schemaComponent-collapse)

<element name="elementType"\>
   <complexType\>
      <complexContent\>
         <extension base="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[baseType](#type_baseType "Jump to "baseType" type definition.")"\>
            <sequence\>
               <element ref="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[enumeration](#element_enumeration "Jump to "enumeration" element declaration.")" minOccurs="0"/>
               <element name="version" minOccurs="0" maxOccurs="unbounded"\>
                  <complexType\>
                     <sequence\>
                        <element ref="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[enumeration](#element_enumeration "Jump to "enumeration" element declaration.")" minOccurs="0"/>
                     </sequence>
                     <attributeGroup ref="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[versionAttributeGroup](#attributeGroup_versionAttributeGroup "Jump to "versionAttributeGroup" attribute group definition.")"/>
                     <attributeGroup ref="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[lengthAttributeGroup](#attributeGroup_lengthAttributeGroup "Jump to "lengthAttributeGroup" attribute group definition.")"/>
                  </complexType>
               </element>
            </sequence>
            <attribute name="name" type="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[nameType](#type_nameType "Jump to "nameType" type definition.")" use="required"/>
            <attribute name="code" type="NMTOKEN" use="optional"/>
            <attribute name="number"\>
               <simpleType\>
                  <restriction base="nonNegativeInteger"\>
                     <minInclusive value="1"/>
                     <maxInclusive value="9999"/>
                  </restriction>
               </simpleType>
            </attribute>
            <attribute name="base" type="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[elementBaseType](#type_elementBaseType "Jump to "elementBaseType" type definition.")" use="optional" default="string"/>
            <attribute name="scale" type="nonNegativeInteger" use="optional" default="0"/>
            <attributeGroup ref="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[lengthAttributeGroup](#attributeGroup_lengthAttributeGroup "Jump to "lengthAttributeGroup" attribute group definition.")"/>
         </extension>
      </complexContent>
   </complexType>
</element>

[](#top "Go to top of page")

* * *

### Element: enumeration

#### [Properties](#element_enumeration-properties-table-collapse)

Name

enumeration

Type

Locally-defined complex type

[Nillable](#term_Nillable "Look up 'Nillable' in glossary")

no

[Abstract](#term_Abstract "Look up 'Abstract' in glossary")

no

#### [Documentation](#element_enumeration-doc-panel-collapse)

No documentation provided.

#### [XML Instance Representation](#element_enumeration-instance-table-collapse)

<[tns](#ns_tns "Find out namespace of 'tns' prefix"):enumeration\>
   <[tns](#ns_tns "Find out namespace of 'tns' prefix"):value
    title="string" \[0..1\]
   \> \[1..\*\] 
       token
   </[tns](#ns_tns "Find out namespace of 'tns' prefix"):value>
</[tns](#ns_tns "Find out namespace of 'tns' prefix"):enumeration>

#### [Schema Component Representation](#element_enumeration-schemaComponent-collapse)

<element name="enumeration"\>
   <complexType\>
      <sequence\>
         <element name="value" maxOccurs="unbounded"\>
            <complexType\>
               <simpleContent\>
                  <extension base="token"\>
                     <attribute name="title" type="string"/>
                  </extension>
               </simpleContent>
            </complexType>
         </element>
      </sequence>
   </complexType>
</element>

[](#top "Go to top of page")

* * *

### Element: implementation

#### [Properties](#element_implementation-properties-table-collapse)

Name

implementation

Type

Locally-defined complex type

[Nillable](#term_Nillable "Look up 'Nillable' in glossary")

no

[Abstract](#term_Abstract "Look up 'Abstract' in glossary")

no

#### [Documentation](#element_implementation-doc-panel-collapse)

No documentation provided.

#### [XML Instance Representation](#element_implementation-instance-table-collapse)

<[tns](#ns_tns "Find out namespace of 'tns' prefix"):implementation
 title="string" \[0..1\]
\>
   <[tns](#ns_tns "Find out namespace of 'tns' prefix"):[description](#element_description "Jump to "description" element declaration.")\> ... </[tns](#ns_tns "Find out namespace of 'tns' prefix"):[description](#element_description "Jump to "description" element declaration.")\> \[0..1\]
   <[tns](#ns_tns "Find out namespace of 'tns' prefix"):sequence   \> \[1\]  
      Start [Choice](#term_Choice "Look up 'Choice' in glossary") \[1..\*\]
         <[tns](#ns_tns "Find out namespace of 'tns' prefix"):segment> [tns](#ns_tns "Find out namespace of 'tns' prefix"):[segmentImpl](#type_segmentImpl "Jump to "segmentImpl" type definition.") </[tns](#ns_tns "Find out namespace of 'tns' prefix"):segment> \[1\]
         <[tns](#ns_tns "Find out namespace of 'tns' prefix"):loop> [tns](#ns_tns "Find out namespace of 'tns' prefix"):[loopImpl](#type_loopImpl "Jump to "loopImpl" type definition.") </[tns](#ns_tns "Find out namespace of 'tns' prefix"):loop> \[0..1\]
      End Choice
   </[tns](#ns_tns "Find out namespace of 'tns' prefix"):sequence>
</[tns](#ns_tns "Find out namespace of 'tns' prefix"):implementation>

#### [Schema Component Representation](#element_implementation-schemaComponent-collapse)

<element name="implementation"\>
   <complexType\>
      <complexContent\>
         <extension base="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[baseType](#type_baseType "Jump to "baseType" type definition.")"\>
            <sequence\>
               <element name="sequence"\>
                  <complexType\>
                     <choice maxOccurs="unbounded"\>
                        <element name="segment" type="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[segmentImpl](#type_segmentImpl "Jump to "segmentImpl" type definition.")"/>
                        <element name="loop" type="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[loopImpl](#type_loopImpl "Jump to "loopImpl" type definition.")" minOccurs="0"/>
                     </choice>
                  </complexType>
               </element>
            </sequence>
         </extension>
      </complexContent>
   </complexType>
</element>

[](#top "Go to top of page")

* * *

### Element: include

#### [Properties](#element_include-properties-table-collapse)

Name

include

Type

Locally-defined complex type

[Nillable](#term_Nillable "Look up 'Nillable' in glossary")

no

[Abstract](#term_Abstract "Look up 'Abstract' in glossary")

no

#### [Documentation](#element_include-doc-panel-collapse)

No documentation provided.

#### [XML Instance Representation](#element_include-instance-table-collapse)

<[tns](#ns_tns "Find out namespace of 'tns' prefix"):include
 schemaLocation="anyURI" \[1\]
/> 

#### [Schema Component Representation](#element_include-schemaComponent-collapse)

<element name="include"\>
   <complexType\>
      <attribute name="schemaLocation" type="anyURI" use="required"/>
   </complexType>
</element>

[](#top "Go to top of page")

* * *

### Element: interchange

#### [Properties](#element_interchange-properties-table-collapse)

Name

interchange

Type

Locally-defined complex type

[Nillable](#term_Nillable "Look up 'Nillable' in glossary")

no

[Abstract](#term_Abstract "Look up 'Abstract' in glossary")

no

#### [Documentation](#element_interchange-doc-panel-collapse)

No documentation provided.

#### [XML Instance Representation](#element_interchange-instance-table-collapse)

<[tns](#ns_tns "Find out namespace of 'tns' prefix"):interchange
 title="string" \[0..1\]
 header="NCName" \[1\]
 trailer="NCName" \[1\]
\>
   <[tns](#ns_tns "Find out namespace of 'tns' prefix"):[description](#element_description "Jump to "description" element declaration.")\> ... </[tns](#ns_tns "Find out namespace of 'tns' prefix"):[description](#element_description "Jump to "description" element declaration.")\> \[0..1\]
   <[tns](#ns_tns "Find out namespace of 'tns' prefix"):sequence   \> \[1\] 
      <[tns](#ns_tns "Find out namespace of 'tns' prefix"):segment> [tns](#ns_tns "Find out namespace of 'tns' prefix"):[segmentStandard](#type_segmentStandard "Jump to "segmentStandard" type definition.") </[tns](#ns_tns "Find out namespace of 'tns' prefix"):segment> \[0..\*\]
      <[tns](#ns_tns "Find out namespace of 'tns' prefix"):group> [tns](#ns_tns "Find out namespace of 'tns' prefix"):[groupControlType](#type_groupControlType "Jump to "groupControlType" type definition.") </[tns](#ns_tns "Find out namespace of 'tns' prefix"):group> \[0..1\]
      <[tns](#ns_tns "Find out namespace of 'tns' prefix"):transaction> [tns](#ns_tns "Find out namespace of 'tns' prefix"):[transactionControlType](#type_transactionControlType "Jump to "transactionControlType" type definition.") </[tns](#ns_tns "Find out namespace of 'tns' prefix"):transaction> \[0..1\]
   </[tns](#ns_tns "Find out namespace of 'tns' prefix"):sequence>
   <[tns](#ns_tns "Find out namespace of 'tns' prefix"):[syntax](#element_syntax "Jump to "syntax" element declaration.")\> ... </[tns](#ns_tns "Find out namespace of 'tns' prefix"):[syntax](#element_syntax "Jump to "syntax" element declaration.")\> \[0..\*\]
</[tns](#ns_tns "Find out namespace of 'tns' prefix"):interchange>

#### [Schema Component Representation](#element_interchange-schemaComponent-collapse)

<element name="interchange"\>
   <complexType\>
      <complexContent\>
         <extension base="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[controlType](#type_controlType "Jump to "controlType" type definition.")"\>
            <sequence\>
               <element name="sequence"\>
                  <complexType\>
                     <sequence\>
                        <element name="segment" type="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[segmentStandard](#type_segmentStandard "Jump to "segmentStandard" type definition.")" minOccurs="0" maxOccurs="unbounded"/>
                        <element name="group" type="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[groupControlType](#type_groupControlType "Jump to "groupControlType" type definition.")" minOccurs="0"/>
                        <element name="transaction" type="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[transactionControlType](#type_transactionControlType "Jump to "transactionControlType" type definition.")" minOccurs="0"/>
                     </sequence>
                  </complexType>
               </element>
               <element ref="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[syntax](#element_syntax "Jump to "syntax" element declaration.")" minOccurs="0" maxOccurs="unbounded"/>
            </sequence>
         </extension>
      </complexContent>
   </complexType>
</element>

[](#top "Go to top of page")

* * *

### Element: schema

#### [Properties](#element_schema-properties-table-collapse)

Name

schema

Type

Locally-defined complex type

[Nillable](#term_Nillable "Look up 'Nillable' in glossary")

no

[Abstract](#term_Abstract "Look up 'Abstract' in glossary")

no

#### [Documentation](#element_schema-doc-panel-collapse)

No documentation provided.

#### [XML Instance Representation](#element_schema-instance-table-collapse)

<[tns](#ns_tns "Find out namespace of 'tns' prefix"):schema\>

×

#### Element include

Optional reference to another schema file to include.

Close

   <[tns](#ns_tns "Find out namespace of 'tns' prefix"):[include](#element_include "Jump to "include" element declaration.")\> ... </[tns](#ns_tns "Find out namespace of 'tns' prefix"):[include](#element_include "Jump to "include" element declaration.")\> \[0..\*\] 
   Start [Choice](#term_Choice "Look up 'Choice' in glossary") \[0..1\]
      <[tns](#ns_tns "Find out namespace of 'tns' prefix"):[interchange](#element_interchange "Jump to "interchange" element declaration.")\> ... </[tns](#ns_tns "Find out namespace of 'tns' prefix"):[interchange](#element_interchange "Jump to "interchange" element declaration.")\> \[1\]
      <[tns](#ns_tns "Find out namespace of 'tns' prefix"):[transaction](#element_transaction "Jump to "transaction" element declaration.")\> ... </[tns](#ns_tns "Find out namespace of 'tns' prefix"):[transaction](#element_transaction "Jump to "transaction" element declaration.")\> \[1\]
      <[tns](#ns_tns "Find out namespace of 'tns' prefix"):[implementation](#element_implementation "Jump to "implementation" element declaration.")\> ... </[tns](#ns_tns "Find out namespace of 'tns' prefix"):[implementation](#element_implementation "Jump to "implementation" element declaration.")\> \[0..1\]
      <[tns](#ns_tns "Find out namespace of 'tns' prefix"):[implementation](#element_implementation "Jump to "implementation" element declaration.")\> ... </[tns](#ns_tns "Find out namespace of 'tns' prefix"):[implementation](#element_implementation "Jump to "implementation" element declaration.")\> \[1\]
   End Choice
   Start [Choice](#term_Choice "Look up 'Choice' in glossary") \[1..\*\]
      <[tns](#ns_tns "Find out namespace of 'tns' prefix"):[elementType](#element_elementType "Jump to "elementType" element declaration.")\> ... </[tns](#ns_tns "Find out namespace of 'tns' prefix"):[elementType](#element_elementType "Jump to "elementType" element declaration.")\> \[1..\*\]
      <[tns](#ns_tns "Find out namespace of 'tns' prefix"):[compositeType](#element_compositeType "Jump to "compositeType" element declaration.")\> ... </[tns](#ns_tns "Find out namespace of 'tns' prefix"):[compositeType](#element_compositeType "Jump to "compositeType" element declaration.")\> \[0..\*\]
      <[tns](#ns_tns "Find out namespace of 'tns' prefix"):[segmentType](#element_segmentType "Jump to "segmentType" element declaration.")\> ... </[tns](#ns_tns "Find out namespace of 'tns' prefix"):[segmentType](#element_segmentType "Jump to "segmentType" element declaration.")\> \[1..\*\]
   End Choice
</[tns](#ns_tns "Find out namespace of 'tns' prefix"):schema>

#### [Schema Component Representation](#element_schema-schemaComponent-collapse)

<element name="schema"\>
   <complexType\>
      <sequence\>
         <element ref="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[include](#element_include "Jump to "include" element declaration.")" minOccurs="0" maxOccurs="unbounded"/>
         <choice minOccurs="0"\>
            <element ref="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[interchange](#element_interchange "Jump to "interchange" element declaration.")"/>
            <sequence\>
               <element ref="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[transaction](#element_transaction "Jump to "transaction" element declaration.")"/>
               <element ref="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[implementation](#element_implementation "Jump to "implementation" element declaration.")" minOccurs="0"/>
            </sequence>
            <sequence\>
               <element ref="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[implementation](#element_implementation "Jump to "implementation" element declaration.")"/>
            </sequence>
         </choice>
         <choice id="typeChoice" maxOccurs="unbounded"\>
            <element ref="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[elementType](#element_elementType "Jump to "elementType" element declaration.")" maxOccurs="unbounded"/>
            <element ref="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[compositeType](#element_compositeType "Jump to "compositeType" element declaration.")" minOccurs="0" maxOccurs="unbounded"/>
            <element ref="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[segmentType](#element_segmentType "Jump to "segmentType" element declaration.")" maxOccurs="unbounded"/>
         </choice>
      </sequence>
   </complexType>
</element>

[](#top "Go to top of page")

* * *

### Element: segmentType

#### [Properties](#element_segmentType-properties-table-collapse)

Name

segmentType

Type

Locally-defined complex type

[Nillable](#term_Nillable "Look up 'Nillable' in glossary")

no

[Abstract](#term_Abstract "Look up 'Abstract' in glossary")

no

#### [Documentation](#element_segmentType-doc-panel-collapse)

Used to declare a segment

#### [XML Instance Representation](#element_segmentType-instance-table-collapse)

<[tns](#ns_tns "Find out namespace of 'tns' prefix"):segmentType
 title="string" \[0..1\]
 name="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[nameType](#type_nameType "Jump to "nameType" type definition.") (_length_ <= 3)" \[1\]

×

#### Attribute name

                Name of the segment. Also referred to as the segment's tag. This is the two or three
                character string used to identify a segment.
              

Close

 
\>
   <[tns](#ns_tns "Find out namespace of 'tns' prefix"):[description](#element_description "Jump to "description" element declaration.")\> ... </[tns](#ns_tns "Find out namespace of 'tns' prefix"):[description](#element_description "Jump to "description" element declaration.")\> \[0..1\]
   <[tns](#ns_tns "Find out namespace of 'tns' prefix"):sequence   \> \[0..1\]  
      Start [Choice](#term_Choice "Look up 'Choice' in glossary") \[0..\*\]
         <[tns](#ns_tns "Find out namespace of 'tns' prefix"):element> [tns](#ns_tns "Find out namespace of 'tns' prefix"):[elementStandard](#type_elementStandard "Jump to "elementStandard" type definition.") </[tns](#ns_tns "Find out namespace of 'tns' prefix"):element> \[1\] 
         <[tns](#ns_tns "Find out namespace of 'tns' prefix"):composite> [tns](#ns_tns "Find out namespace of 'tns' prefix"):[compositeStandard](#type_compositeStandard "Jump to "compositeStandard" type definition.") </[tns](#ns_tns "Find out namespace of 'tns' prefix"):composite> \[1\]
         <[tns](#ns_tns "Find out namespace of 'tns' prefix"):any> [tns](#ns_tns "Find out namespace of 'tns' prefix"):[anyElementType](#type_anyElementType "Jump to "anyElementType" type definition.") </[tns](#ns_tns "Find out namespace of 'tns' prefix"):any> \[1\] 
      End Choice
   </[tns](#ns_tns "Find out namespace of 'tns' prefix"):sequence>
   <[tns](#ns_tns "Find out namespace of 'tns' prefix"):[syntax](#element_syntax "Jump to "syntax" element declaration.")\> ... </[tns](#ns_tns "Find out namespace of 'tns' prefix"):[syntax](#element_syntax "Jump to "syntax" element declaration.")\> \[0..\*\]
</[tns](#ns_tns "Find out namespace of 'tns' prefix"):segmentType>

#### [Schema Component Representation](#element_segmentType-schemaComponent-collapse)

<element name="segmentType"\>
   <complexType\>
      <complexContent\>
         <extension base="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[baseType](#type_baseType "Jump to "baseType" type definition.")"\>
            <sequence\>
               <element name="sequence" minOccurs="0"\>
                  <complexType\>
                     <choice minOccurs="0" maxOccurs="unbounded"\>
                        <element name="element" type="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[elementStandard](#type_elementStandard "Jump to "elementStandard" type definition.")"/>
                        <element name="composite" type="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[compositeStandard](#type_compositeStandard "Jump to "compositeStandard" type definition.")"/>
                        <element name="any" type="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[anyElementType](#type_anyElementType "Jump to "anyElementType" type definition.")"/>
                     </choice>
                  </complexType>
               </element>
               <element ref="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[syntax](#element_syntax "Jump to "syntax" element declaration.")" minOccurs="0" maxOccurs="unbounded"/>
            </sequence>
            <attribute name="name" use="required"\>
               <simpleType\>
                  <restriction base="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[nameType](#type_nameType "Jump to "nameType" type definition.")"\>
                     <maxLength value="3"/>
                  </restriction>
               </simpleType>
            </attribute>
         </extension>
      </complexContent>
   </complexType>
</element>

[](#top "Go to top of page")

* * *

### Element: syntax

#### [Properties](#element_syntax-properties-table-collapse)

Name

syntax

Type

Locally-defined complex type

[Nillable](#term_Nillable "Look up 'Nillable' in glossary")

no

[Abstract](#term_Abstract "Look up 'Abstract' in glossary")

no

#### [Documentation](#element_syntax-doc-panel-collapse)

No documentation provided.

#### [XML Instance Representation](#element_syntax-instance-table-collapse)

<[tns](#ns_tns "Find out namespace of 'tns' prefix"):syntax
 type="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[syntaxType](#type_syntaxType "Jump to "syntaxType" type definition.")" \[0..1\]
\>
   <[tns](#ns_tns "Find out namespace of 'tns' prefix"):position> [tns](#ns_tns "Find out namespace of 'tns' prefix"):[positionType](#type_positionType "Jump to "positionType" type definition.") </[tns](#ns_tns "Find out namespace of 'tns' prefix"):position> \[1..\*\]
</[tns](#ns_tns "Find out namespace of 'tns' prefix"):syntax>

#### [Schema Component Representation](#element_syntax-schemaComponent-collapse)

<element name="syntax"\>
   <complexType\>
      <sequence\>
         <element name="position" type="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[positionType](#type_positionType "Jump to "positionType" type definition.")" maxOccurs="unbounded"/>
      </sequence>
      <attribute name="type" type="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[syntaxType](#type_syntaxType "Jump to "syntaxType" type definition.")"/>
   </complexType>
</element>

[](#top "Go to top of page")

* * *

### Element: transaction

#### [Properties](#element_transaction-properties-table-collapse)

Name

transaction

Type

Locally-defined complex type

[Nillable](#term_Nillable "Look up 'Nillable' in glossary")

no

[Abstract](#term_Abstract "Look up 'Abstract' in glossary")

no

#### [Documentation](#element_transaction-doc-panel-collapse)

No documentation provided.

#### [XML Instance Representation](#element_transaction-instance-table-collapse)

<[tns](#ns_tns "Find out namespace of 'tns' prefix"):transaction
 title="string" \[0..1\]
\>
   <[tns](#ns_tns "Find out namespace of 'tns' prefix"):[description](#element_description "Jump to "description" element declaration.")\> ... </[tns](#ns_tns "Find out namespace of 'tns' prefix"):[description](#element_description "Jump to "description" element declaration.")\> \[0..1\]
   <[tns](#ns_tns "Find out namespace of 'tns' prefix"):sequence   \> \[1\]  
      Start [Choice](#term_Choice "Look up 'Choice' in glossary") \[1..\*\]
         <[tns](#ns_tns "Find out namespace of 'tns' prefix"):segment> [tns](#ns_tns "Find out namespace of 'tns' prefix"):[segmentStandard](#type_segmentStandard "Jump to "segmentStandard" type definition.") </[tns](#ns_tns "Find out namespace of 'tns' prefix"):segment> \[1\]
         <[tns](#ns_tns "Find out namespace of 'tns' prefix"):loop> [tns](#ns_tns "Find out namespace of 'tns' prefix"):[loopStandard](#type_loopStandard "Jump to "loopStandard" type definition.") </[tns](#ns_tns "Find out namespace of 'tns' prefix"):loop> \[0..1\]
      End Choice
   </[tns](#ns_tns "Find out namespace of 'tns' prefix"):sequence>
   <[tns](#ns_tns "Find out namespace of 'tns' prefix"):[syntax](#element_syntax "Jump to "syntax" element declaration.")\> ... </[tns](#ns_tns "Find out namespace of 'tns' prefix"):[syntax](#element_syntax "Jump to "syntax" element declaration.")\> \[0..\*\]
</[tns](#ns_tns "Find out namespace of 'tns' prefix"):transaction>

#### [Schema Component Representation](#element_transaction-schemaComponent-collapse)

<element name="transaction"\>
   <complexType\>
      <complexContent\>
         <extension base="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[baseType](#type_baseType "Jump to "baseType" type definition.")"\>
            <sequence\>
               <element name="sequence"\>
                  <complexType\>
                     <choice maxOccurs="unbounded"\>
                        <element name="segment" type="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[segmentStandard](#type_segmentStandard "Jump to "segmentStandard" type definition.")"/>
                        <element name="loop" type="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[loopStandard](#type_loopStandard "Jump to "loopStandard" type definition.")" minOccurs="0"/>
                     </choice>
                  </complexType>
               </element>
               <element ref="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[syntax](#element_syntax "Jump to "syntax" element declaration.")" minOccurs="0" maxOccurs="unbounded"/>
            </sequence>
         </extension>
      </complexContent>
   </complexType>
</element>

[](#top "Go to top of page")

* * *

Global Definitions
------------------

### Attribute Group: implementationAttributeGroup

#### [Properties](#attributeGroup_implementationAttributeGroup-properties-table-collapse)

Name

implementationAttributeGroup

#### [Documentation](#attributeGroup_implementationAttributeGroup-doc-panel-collapse)

No documentation provided.

#### [XML Instance Representation](#attributeGroup_implementationAttributeGroup-instance-table-collapse)

minOccurs="nonNegativeInteger" \[0..1\]

×

#### Attribute minOccurs

          The minimum number of times a type may occur at the declared location
          in the EDI structure.
        

Close

 
maxOccurs="nonNegativeInteger" \[0..1\]

×

#### Attribute maxOccurs

          The maximum number of times a type may occur at the declared location
          in the EDI structure.
        

Close

 

#### [Schema Component Representation](#attributeGroup_implementationAttributeGroup-schemaComponent-collapse)

<attributeGroup name="implementationAttributeGroup"\>
   <attribute name="minOccurs" type="nonNegativeInteger"/>
   <attribute name="maxOccurs" type="nonNegativeInteger"/>
</attributeGroup>

[](#top "Go to top of page")

* * *

### Attribute Group: lengthAttributeGroup

#### [Properties](#attributeGroup_lengthAttributeGroup-properties-table-collapse)

Name

lengthAttributeGroup

#### [Documentation](#attributeGroup_lengthAttributeGroup-doc-panel-collapse)

No documentation provided.

#### [XML Instance Representation](#attributeGroup_lengthAttributeGroup-instance-table-collapse)

minLength="nonNegativeInteger" \[0..1\]

×

#### Attribute minLength

          The minimum length allowed for an element value to be valid.
        

Close

 
maxLength="nonNegativeInteger" \[0..1\]

×

#### Attribute maxLength

          The maximum length allowed for an element value to be valid.
        

Close

 

#### [Schema Component Representation](#attributeGroup_lengthAttributeGroup-schemaComponent-collapse)

<attributeGroup name="lengthAttributeGroup"\>
   <attribute name="minLength" type="nonNegativeInteger" default="1"/>
   <attribute name="maxLength" type="nonNegativeInteger" default="1"/>
</attributeGroup>

[](#top "Go to top of page")

* * *

### Attribute Group: occursAttributeGroup

#### [Properties](#attributeGroup_occursAttributeGroup-properties-table-collapse)

Name

occursAttributeGroup

#### [Documentation](#attributeGroup_occursAttributeGroup-doc-panel-collapse)

No documentation provided.

#### [XML Instance Representation](#attributeGroup_occursAttributeGroup-instance-table-collapse)

minOccurs="nonNegativeInteger" \[0..1\]

×

#### Attribute minOccurs

          The minimum number of times a type may occur at the declared location
          in the EDI structure.
        

Close

 
maxOccurs="nonNegativeInteger" \[0..1\]

×

#### Attribute maxOccurs

          The maximum number of times a type may occur at the declared location
          in the EDI structure.
        

Close

 

#### [Schema Component Representation](#attributeGroup_occursAttributeGroup-schemaComponent-collapse)

<attributeGroup name="occursAttributeGroup"\>
   <attribute name="minOccurs" type="nonNegativeInteger" default="0"/>
   <attribute name="maxOccurs" type="nonNegativeInteger" default="1"/>
</attributeGroup>

[](#top "Go to top of page")

* * *

### Attribute Group: referenceAttributeGroup

#### [Properties](#attributeGroup_referenceAttributeGroup-properties-table-collapse)

Name

referenceAttributeGroup

#### [Documentation](#attributeGroup_referenceAttributeGroup-doc-panel-collapse)

No documentation provided.

#### [XML Instance Representation](#attributeGroup_referenceAttributeGroup-instance-table-collapse)

type="NCName" \[0..1\]

×

#### Attribute type

          The name of the target type being referenced.
        

Close

 
minOccurs="nonNegativeInteger" \[0..1\]

×

#### Attribute minOccurs

          The minimum number of times a type may occur at the declared location
          in the EDI structure.
        

Close

 
maxOccurs="nonNegativeInteger" \[0..1\]

×

#### Attribute maxOccurs

          The maximum number of times a type may occur at the declared location
          in the EDI structure.
        

Close

 

#### [Schema Component Representation](#attributeGroup_referenceAttributeGroup-schemaComponent-collapse)

<attributeGroup name="referenceAttributeGroup"\>
   <attribute name="type" type="NCName"/>
   <attributeGroup ref="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[occursAttributeGroup](#attributeGroup_occursAttributeGroup "Jump to "occursAttributeGroup" attribute group definition.")"/>
</attributeGroup>

[](#top "Go to top of page")

* * *

### Attribute Group: versionAttributeGroup

#### [Properties](#attributeGroup_versionAttributeGroup-properties-table-collapse)

Name

versionAttributeGroup

#### [Documentation](#attributeGroup_versionAttributeGroup-doc-panel-collapse)

No documentation provided.

#### [XML Instance Representation](#attributeGroup_versionAttributeGroup-instance-table-collapse)

minVersion="token" \[0..1\]

×

#### Attribute minVersion

          The minimum transaction version this schema version applies to.
        

Close

 
maxVersion="token" \[0..1\]

×

#### Attribute maxVersion

          The maximum transaction version this schema version applies to.
        

Close

 

#### [Schema Component Representation](#attributeGroup_versionAttributeGroup-schemaComponent-collapse)

<attributeGroup name="versionAttributeGroup"\>
   <attribute name="minVersion" type="token"/>
   <attribute name="maxVersion" type="token"/>
</attributeGroup>

[](#top "Go to top of page")

* * *

### Complex Type: anyElementType

#### [Type hierarchy](#type_anyElementType-type-hierarchy-collapse)

Super-types:

[baseType](#type_baseType "Jump to "baseType" type definition.") < **anyElementType** (by extension)

Sub-types:

None

#### [Properties](#type_anyElementType-properties-table-collapse)

Name

anyElementType

[Abstract](#term_Abstract "Look up 'Abstract' in glossary")

no

#### [Documentation](#type_anyElementType-doc-panel-collapse)

No documentation provided.

#### [XML Instance Representation](#type_anyElementType-instance-table-collapse)

<...
 title="string" \[0..1\]
 minOccurs="nonNegativeInteger" \[0..1\]

×

#### Attribute minOccurs

The minimum number of times an undefined element may occur at the declared location in the EDI structure.

Close

 
 maxOccurs="nonNegativeInteger" \[0..1\]

×

#### Attribute maxOccurs

The maximum number of times an undefined element may occur at the declared location in the EDI structure.

Close

 
\>
   <[tns](#ns_tns "Find out namespace of 'tns' prefix"):[description](#element_description "Jump to "description" element declaration.")\> ... </[tns](#ns_tns "Find out namespace of 'tns' prefix"):[description](#element_description "Jump to "description" element declaration.")\> \[0..1\]
</...>

#### [Schema Component Representation](#type_anyElementType-schemaComponent-collapse)

<complexType name="anyElementType"\>
   <complexContent\>
      <extension base="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[baseType](#type_baseType "Jump to "baseType" type definition.")"\>
         <attribute name="minOccurs" type="nonNegativeInteger" default="0"/>
         <attribute name="maxOccurs" type="nonNegativeInteger" default="1"/>
      </extension>
   </complexContent>
</complexType>

[](#top "Go to top of page")

* * *

### Complex Type: baseType

#### [Type hierarchy](#type_baseType-type-hierarchy-collapse)

Super-types:

None

Sub-types:

*   [anyElementType](#type_anyElementType "Jump to "anyElementType" type definition.") (by extension)
*   [controlType](#type_controlType "Jump to "controlType" type definition.") (by extension)
    *   [transactionControlType](#type_transactionControlType "Jump to "transactionControlType" type definition.") (by extension)
    *   [groupControlType](#type_groupControlType "Jump to "groupControlType" type definition.") (by extension)
*   [elementStandard](#type_elementStandard "Jump to "elementStandard" type definition.") (by extension)
*   [elementImpl](#type_elementImpl "Jump to "elementImpl" type definition.") (by extension)
*   [compositeStandard](#type_compositeStandard "Jump to "compositeStandard" type definition.") (by extension)
*   [compositeImpl](#type_compositeImpl "Jump to "compositeImpl" type definition.") (by extension)
*   [segmentStandard](#type_segmentStandard "Jump to "segmentStandard" type definition.") (by extension)
*   [segmentImpl](#type_segmentImpl "Jump to "segmentImpl" type definition.") (by extension)
*   [loopBase](#type_loopBase "Jump to "loopBase" type definition.") (by extension)
    *   [loopStandard](#type_loopStandard "Jump to "loopStandard" type definition.") (by extension)
    *   [loopImpl](#type_loopImpl "Jump to "loopImpl" type definition.") (by extension)

#### [Properties](#type_baseType-properties-table-collapse)

Name

baseType

[Abstract](#term_Abstract "Look up 'Abstract' in glossary")

yes

#### [Documentation](#type_baseType-doc-panel-collapse)

No documentation provided.

#### [XML Instance Representation](#type_baseType-instance-table-collapse)

<...
 title="string" \[0..1\]
\>
   <[tns](#ns_tns "Find out namespace of 'tns' prefix"):[description](#element_description "Jump to "description" element declaration.")\> ... </[tns](#ns_tns "Find out namespace of 'tns' prefix"):[description](#element_description "Jump to "description" element declaration.")\> \[0..1\]
</...>

#### [Schema Component Representation](#type_baseType-schemaComponent-collapse)

<complexType name="baseType" abstract="true"\>
   <sequence\>
      <element ref="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[description](#element_description "Jump to "description" element declaration.")" minOccurs="0" maxOccurs="1"/>
   </sequence>
   <attribute name="title" type="string" use="optional"/>
</complexType>

[](#top "Go to top of page")

* * *

### Complex Type: compositeImpl

#### [Type hierarchy](#type_compositeImpl-type-hierarchy-collapse)

Super-types:

[baseType](#type_baseType "Jump to "baseType" type definition.") < **compositeImpl** (by extension)

Sub-types:

None

#### [Properties](#type_compositeImpl-properties-table-collapse)

Name

compositeImpl

[Abstract](#term_Abstract "Look up 'Abstract' in glossary")

no

#### [Documentation](#type_compositeImpl-doc-panel-collapse)

No documentation provided.

#### [XML Instance Representation](#type_compositeImpl-instance-table-collapse)

<...
 title="string" \[0..1\]
 position="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[positionType](#type_positionType "Jump to "positionType" type definition.")" \[1\]
 minOccurs="nonNegativeInteger" \[0..1\]

×

#### Attribute minOccurs

          The minimum number of times a type may occur at the declared location
          in the EDI structure.
        

Close

 
 maxOccurs="nonNegativeInteger" \[0..1\]

×

#### Attribute maxOccurs

          The maximum number of times a type may occur at the declared location
          in the EDI structure.
        

Close

 
\>
   <[tns](#ns_tns "Find out namespace of 'tns' prefix"):[description](#element_description "Jump to "description" element declaration.")\> ... </[tns](#ns_tns "Find out namespace of 'tns' prefix"):[description](#element_description "Jump to "description" element declaration.")\> \[0..1\]
   <[tns](#ns_tns "Find out namespace of 'tns' prefix"):sequence   \> \[0..1\]  
      <[tns](#ns_tns "Find out namespace of 'tns' prefix"):element> [tns](#ns_tns "Find out namespace of 'tns' prefix"):[elementImpl](#type_elementImpl "Jump to "elementImpl" type definition.") </[tns](#ns_tns "Find out namespace of 'tns' prefix"):element> \[1..\*\]
   </[tns](#ns_tns "Find out namespace of 'tns' prefix"):sequence>
</...>

#### [Schema Component Representation](#type_compositeImpl-schemaComponent-collapse)

<complexType name="compositeImpl"\>
   <complexContent\>
      <extension base="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[baseType](#type_baseType "Jump to "baseType" type definition.")"\>
         <sequence\>
            <element name="sequence" minOccurs="0"\>
               <complexType\>
                  <sequence\>
                     <element name="element" type="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[elementImpl](#type_elementImpl "Jump to "elementImpl" type definition.")" minOccurs="1" maxOccurs="unbounded"/>
                  </sequence>
               </complexType>
            </element>
         </sequence>
         <attribute name="position" type="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[positionType](#type_positionType "Jump to "positionType" type definition.")" use="required"/>
         <attributeGroup ref="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[implementationAttributeGroup](#attributeGroup_implementationAttributeGroup "Jump to "implementationAttributeGroup" attribute group definition.")"/>
      </extension>
   </complexContent>
</complexType>

[](#top "Go to top of page")

* * *

### Complex Type: compositeStandard

#### [Type hierarchy](#type_compositeStandard-type-hierarchy-collapse)

Super-types:

[baseType](#type_baseType "Jump to "baseType" type definition.") < **compositeStandard** (by extension)

Sub-types:

None

#### [Properties](#type_compositeStandard-properties-table-collapse)

Name

compositeStandard

[Abstract](#term_Abstract "Look up 'Abstract' in glossary")

no

#### [Documentation](#type_compositeStandard-doc-panel-collapse)

No documentation provided.

#### [XML Instance Representation](#type_compositeStandard-instance-table-collapse)

<...
 title="string" \[0..1\]
 type="NCName" \[0..1\]

×

#### Attribute type

          The name of the target type being referenced.
        

Close

 
 minOccurs="nonNegativeInteger" \[0..1\]

×

#### Attribute minOccurs

          The minimum number of times a type may occur at the declared location
          in the EDI structure.
        

Close

 
 maxOccurs="nonNegativeInteger" \[0..1\]

×

#### Attribute maxOccurs

          The maximum number of times a type may occur at the declared location
          in the EDI structure.
        

Close

 
\>
   <[tns](#ns_tns "Find out namespace of 'tns' prefix"):[description](#element_description "Jump to "description" element declaration.")\> ... </[tns](#ns_tns "Find out namespace of 'tns' prefix"):[description](#element_description "Jump to "description" element declaration.")\> \[0..1\]
   <[tns](#ns_tns "Find out namespace of 'tns' prefix"):version
    minVersion="token" \[0..1\]

×

#### Attribute minVersion

          The minimum transaction version this schema version applies to.
        

Close

 
    maxVersion="token" \[0..1\]

×

#### Attribute maxVersion

          The maximum transaction version this schema version applies to.
        

Close

 
    minOccurs="nonNegativeInteger" \[0..1\]

×

#### Attribute minOccurs

          The minimum number of times a type may occur at the declared location
          in the EDI structure.
        

Close

 
    maxOccurs="nonNegativeInteger" \[0..1\]

×

#### Attribute maxOccurs

          The maximum number of times a type may occur at the declared location
          in the EDI structure.
        

Close

 
/>  \[0..\*\]

</...>

#### [Schema Component Representation](#type_compositeStandard-schemaComponent-collapse)

<complexType name="compositeStandard"\>
   <complexContent\>
      <extension base="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[baseType](#type_baseType "Jump to "baseType" type definition.")"\>
         <sequence\>
            <element name="version" minOccurs="0" maxOccurs="unbounded"\>
               <complexType\>
                  <attributeGroup ref="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[versionAttributeGroup](#attributeGroup_versionAttributeGroup "Jump to "versionAttributeGroup" attribute group definition.")"/>
                  <attributeGroup ref="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[occursAttributeGroup](#attributeGroup_occursAttributeGroup "Jump to "occursAttributeGroup" attribute group definition.")"/>
               </complexType>
            </element>
         </sequence>
         <attributeGroup ref="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[referenceAttributeGroup](#attributeGroup_referenceAttributeGroup "Jump to "referenceAttributeGroup" attribute group definition.")"/>
      </extension>
   </complexContent>
</complexType>

[](#top "Go to top of page")

* * *

### Complex Type: controlType

#### [Type hierarchy](#type_controlType-type-hierarchy-collapse)

Super-types:

[baseType](#type_baseType "Jump to "baseType" type definition.") < **controlType** (by extension)

Sub-types:

*   [transactionControlType](#type_transactionControlType "Jump to "transactionControlType" type definition.") (by extension)
*   [groupControlType](#type_groupControlType "Jump to "groupControlType" type definition.") (by extension)

#### [Properties](#type_controlType-properties-table-collapse)

Name

controlType

[Abstract](#term_Abstract "Look up 'Abstract' in glossary")

yes

#### [Documentation](#type_controlType-doc-panel-collapse)

No documentation provided.

#### [XML Instance Representation](#type_controlType-instance-table-collapse)

<...
 title="string" \[0..1\]
 header="NCName" \[1\]
 trailer="NCName" \[1\]
\>
   <[tns](#ns_tns "Find out namespace of 'tns' prefix"):[description](#element_description "Jump to "description" element declaration.")\> ... </[tns](#ns_tns "Find out namespace of 'tns' prefix"):[description](#element_description "Jump to "description" element declaration.")\> \[0..1\]
</...>

#### [Schema Component Representation](#type_controlType-schemaComponent-collapse)

<complexType name="controlType" abstract="true"\>
   <complexContent\>
      <extension base="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[baseType](#type_baseType "Jump to "baseType" type definition.")"\>
         <attribute name="header" type="NCName" use="required"/>
         <attribute name="trailer" type="NCName" use="required"/>
      </extension>
   </complexContent>
</complexType>

[](#top "Go to top of page")

* * *

### Complex Type: elementImpl

#### [Type hierarchy](#type_elementImpl-type-hierarchy-collapse)

Super-types:

[baseType](#type_baseType "Jump to "baseType" type definition.") < **elementImpl** (by extension)

Sub-types:

None

#### [Properties](#type_elementImpl-properties-table-collapse)

Name

elementImpl

[Abstract](#term_Abstract "Look up 'Abstract' in glossary")

no

#### [Documentation](#type_elementImpl-doc-panel-collapse)

No documentation provided.

#### [XML Instance Representation](#type_elementImpl-instance-table-collapse)

<...
 title="string" \[0..1\]
 position="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[positionType](#type_positionType "Jump to "positionType" type definition.")" \[1\]
 minOccurs="nonNegativeInteger" \[0..1\]

×

#### Attribute minOccurs

          The minimum number of times a type may occur at the declared location
          in the EDI structure.
        

Close

 
 maxOccurs="nonNegativeInteger" \[0..1\]

×

#### Attribute maxOccurs

          The maximum number of times a type may occur at the declared location
          in the EDI structure.
        

Close

 
\>
   <[tns](#ns_tns "Find out namespace of 'tns' prefix"):[description](#element_description "Jump to "description" element declaration.")\> ... </[tns](#ns_tns "Find out namespace of 'tns' prefix"):[description](#element_description "Jump to "description" element declaration.")\> \[0..1\]
   <[tns](#ns_tns "Find out namespace of 'tns' prefix"):[enumeration](#element_enumeration "Jump to "enumeration" element declaration.")\> ... </[tns](#ns_tns "Find out namespace of 'tns' prefix"):[enumeration](#element_enumeration "Jump to "enumeration" element declaration.")\> \[0..1\]
</...>

#### [Schema Component Representation](#type_elementImpl-schemaComponent-collapse)

<complexType name="elementImpl"\>
   <complexContent\>
      <extension base="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[baseType](#type_baseType "Jump to "baseType" type definition.")"\>
         <sequence\>
            <element ref="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[enumeration](#element_enumeration "Jump to "enumeration" element declaration.")" minOccurs="0"/>
         </sequence>
         <attribute name="position" type="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[positionType](#type_positionType "Jump to "positionType" type definition.")" use="required"/>
         <attributeGroup ref="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[implementationAttributeGroup](#attributeGroup_implementationAttributeGroup "Jump to "implementationAttributeGroup" attribute group definition.")"/>
      </extension>
   </complexContent>
</complexType>

[](#top "Go to top of page")

* * *

### Complex Type: elementStandard

#### [Type hierarchy](#type_elementStandard-type-hierarchy-collapse)

Super-types:

[baseType](#type_baseType "Jump to "baseType" type definition.") < **elementStandard** (by extension)

Sub-types:

None

#### [Properties](#type_elementStandard-properties-table-collapse)

Name

elementStandard

[Abstract](#term_Abstract "Look up 'Abstract' in glossary")

no

#### [Documentation](#type_elementStandard-doc-panel-collapse)

No documentation provided.

#### [XML Instance Representation](#type_elementStandard-instance-table-collapse)

<...
 title="string" \[0..1\]
 type="NCName" \[0..1\]

×

#### Attribute type

          The name of the target type being referenced.
        

Close

 
 minOccurs="nonNegativeInteger" \[0..1\]

×

#### Attribute minOccurs

          The minimum number of times a type may occur at the declared location
          in the EDI structure.
        

Close

 
 maxOccurs="nonNegativeInteger" \[0..1\]

×

#### Attribute maxOccurs

          The maximum number of times a type may occur at the declared location
          in the EDI structure.
        

Close

 
\>
   <[tns](#ns_tns "Find out namespace of 'tns' prefix"):[description](#element_description "Jump to "description" element declaration.")\> ... </[tns](#ns_tns "Find out namespace of 'tns' prefix"):[description](#element_description "Jump to "description" element declaration.")\> \[0..1\]
   <[tns](#ns_tns "Find out namespace of 'tns' prefix"):version
    minVersion="token" \[0..1\]

×

#### Attribute minVersion

          The minimum transaction version this schema version applies to.
        

Close

 
    maxVersion="token" \[0..1\]

×

#### Attribute maxVersion

          The maximum transaction version this schema version applies to.
        

Close

 
    minOccurs="nonNegativeInteger" \[0..1\]

×

#### Attribute minOccurs

          The minimum number of times a type may occur at the declared location
          in the EDI structure.
        

Close

 
    maxOccurs="nonNegativeInteger" \[0..1\]

×

#### Attribute maxOccurs

          The maximum number of times a type may occur at the declared location
          in the EDI structure.
        

Close

 
/>  \[0..\*\]

</...>

#### [Schema Component Representation](#type_elementStandard-schemaComponent-collapse)

<complexType name="elementStandard"\>
   <complexContent\>
      <extension base="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[baseType](#type_baseType "Jump to "baseType" type definition.")"\>
         <sequence\>
            <element name="version" minOccurs="0" maxOccurs="unbounded"\>
               <complexType\>
                  <attributeGroup ref="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[versionAttributeGroup](#attributeGroup_versionAttributeGroup "Jump to "versionAttributeGroup" attribute group definition.")"/>
                  <attributeGroup ref="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[occursAttributeGroup](#attributeGroup_occursAttributeGroup "Jump to "occursAttributeGroup" attribute group definition.")"/>
               </complexType>
            </element>
         </sequence>
         <attributeGroup ref="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[referenceAttributeGroup](#attributeGroup_referenceAttributeGroup "Jump to "referenceAttributeGroup" attribute group definition.")"/>
      </extension>
   </complexContent>
</complexType>

[](#top "Go to top of page")

* * *

### Complex Type: groupControlType

#### [Type hierarchy](#type_groupControlType-type-hierarchy-collapse)

Super-types:

[baseType](#type_baseType "Jump to "baseType" type definition.") < [controlType](#type_controlType "Jump to "controlType" type definition.") (by extension) < **groupControlType** (by extension)

Sub-types:

None

#### [Properties](#type_groupControlType-properties-table-collapse)

Name

groupControlType

[Abstract](#term_Abstract "Look up 'Abstract' in glossary")

no

#### [Documentation](#type_groupControlType-doc-panel-collapse)

No documentation provided.

#### [XML Instance Representation](#type_groupControlType-instance-table-collapse)

<...
 title="string" \[0..1\]
 header="NCName" \[1\]
 trailer="NCName" \[1\]
 use="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[useType](#type_useType "Jump to "useType" type definition.")" \[0..1\]
\>
   <[tns](#ns_tns "Find out namespace of 'tns' prefix"):[description](#element_description "Jump to "description" element declaration.")\> ... </[tns](#ns_tns "Find out namespace of 'tns' prefix"):[description](#element_description "Jump to "description" element declaration.")\> \[0..1\]
   <[tns](#ns_tns "Find out namespace of 'tns' prefix"):transaction> [tns](#ns_tns "Find out namespace of 'tns' prefix"):[transactionControlType](#type_transactionControlType "Jump to "transactionControlType" type definition.") </[tns](#ns_tns "Find out namespace of 'tns' prefix"):transaction> \[0..1\]
</...>

#### [Schema Component Representation](#type_groupControlType-schemaComponent-collapse)

<complexType name="groupControlType"\>
   <complexContent\>
      <extension base="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[controlType](#type_controlType "Jump to "controlType" type definition.")"\>
         <sequence\>
            <element name="transaction" type="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[transactionControlType](#type_transactionControlType "Jump to "transactionControlType" type definition.")" minOccurs="0"/>
         </sequence>
         <attribute name="use" type="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[useType](#type_useType "Jump to "useType" type definition.")" default="optional"/>
      </extension>
   </complexContent>
</complexType>

[](#top "Go to top of page")

* * *

### Complex Type: loopBase

#### [Type hierarchy](#type_loopBase-type-hierarchy-collapse)

Super-types:

[baseType](#type_baseType "Jump to "baseType" type definition.") < **loopBase** (by extension)

Sub-types:

*   [loopStandard](#type_loopStandard "Jump to "loopStandard" type definition.") (by extension)
*   [loopImpl](#type_loopImpl "Jump to "loopImpl" type definition.") (by extension)

#### [Properties](#type_loopBase-properties-table-collapse)

Name

loopBase

[Abstract](#term_Abstract "Look up 'Abstract' in glossary")

yes

#### [Documentation](#type_loopBase-doc-panel-collapse)

No documentation provided.

#### [XML Instance Representation](#type_loopBase-instance-table-collapse)

<...
 title="string" \[0..1\]
 minOccurs="nonNegativeInteger" \[0..1\]

×

#### Attribute minOccurs

              The minimum number of times a loop may repeat. A value of 0 (zero)
              indicates that the loop is optional.

              When used in a loop defined
              within an implementation,
              the value may not be less than the value set on the standard loop referenced
              by the implementation loop's 'type'
              attribute.
            

Close

 
 maxOccurs="nonNegativeInteger" \[0..1\]

×

#### Attribute maxOccurs

              The maximum number of times a loop may repeat.
              When used in a loop defined within an implementation, the value
              may not be greater than
              the value set on the standard loop referenced
              by the implementation loop's 'type' attribute.
            

Close

 
\>
   <[tns](#ns_tns "Find out namespace of 'tns' prefix"):[description](#element_description "Jump to "description" element declaration.")\> ... </[tns](#ns_tns "Find out namespace of 'tns' prefix"):[description](#element_description "Jump to "description" element declaration.")\> \[0..1\]
</...>

#### [Schema Component Representation](#type_loopBase-schemaComponent-collapse)

<complexType name="loopBase" abstract="true"\>
   <complexContent\>
      <extension base="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[baseType](#type_baseType "Jump to "baseType" type definition.")"\>
         <attribute name="minOccurs" type="nonNegativeInteger" default="0"/>
         <attribute name="maxOccurs" type="nonNegativeInteger" default="1"/>
      </extension>
   </complexContent>
</complexType>

[](#top "Go to top of page")

* * *

### Complex Type: loopImpl

#### [Type hierarchy](#type_loopImpl-type-hierarchy-collapse)

Super-types:

[baseType](#type_baseType "Jump to "baseType" type definition.") < [loopBase](#type_loopBase "Jump to "loopBase" type definition.") (by extension) < **loopImpl** (by extension)

Sub-types:

None

#### [Properties](#type_loopImpl-properties-table-collapse)

Name

loopImpl

[Abstract](#term_Abstract "Look up 'Abstract' in glossary")

no

#### [Documentation](#type_loopImpl-doc-panel-collapse)

No documentation provided.

#### [XML Instance Representation](#type_loopImpl-instance-table-collapse)

<...
 title="string" \[0..1\]
 minOccurs="nonNegativeInteger" \[0..1\]

×

#### Attribute minOccurs

              The minimum number of times a loop may repeat. A value of 0 (zero)
              indicates that the loop is optional.

              When used in a loop defined
              within an implementation,
              the value may not be less than the value set on the standard loop referenced
              by the implementation loop's 'type'
              attribute.
            

Close

 
 maxOccurs="nonNegativeInteger" \[0..1\]

×

#### Attribute maxOccurs

              The maximum number of times a loop may repeat.
              When used in a loop defined within an implementation, the value
              may not be greater than
              the value set on the standard loop referenced
              by the implementation loop's 'type' attribute.
            

Close

 
 type="NMTOKEN" \[1\]

×

#### Attribute type

              The identifier (code attribute) of the standard loop this loop
              implements.
            

Close

 
 code="NMTOKEN" \[1\]

×

#### Attribute code

              Code used to uniquely identify a loop implementation within the
              transaction/message implementation.
            

Close

 
 discriminator="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[discriminatorType](#type_discriminatorType "Jump to "discriminatorType" type definition.")" \[0..1\]

×

#### Attribute discriminator

              The element position in the loop's first segment used to identify an
              implementation of a standard loop from other implementations. The
              element identified by the position given in this attribute must also specify an
              enumeration of values used only by this implementation and not used
              by any other implementations of the standard loop at the same level of the
              transaction.
            

Close

 
\>
   <[tns](#ns_tns "Find out namespace of 'tns' prefix"):[description](#element_description "Jump to "description" element declaration.")\> ... </[tns](#ns_tns "Find out namespace of 'tns' prefix"):[description](#element_description "Jump to "description" element declaration.")\> \[0..1\]
   <[tns](#ns_tns "Find out namespace of 'tns' prefix"):sequence   \> \[1\]  
      Start [Choice](#term_Choice "Look up 'Choice' in glossary") \[1..\*\]
         <[tns](#ns_tns "Find out namespace of 'tns' prefix"):segment> [tns](#ns_tns "Find out namespace of 'tns' prefix"):[segmentImpl](#type_segmentImpl "Jump to "segmentImpl" type definition.") </[tns](#ns_tns "Find out namespace of 'tns' prefix"):segment> \[1\]
         <[tns](#ns_tns "Find out namespace of 'tns' prefix"):loop> [tns](#ns_tns "Find out namespace of 'tns' prefix"):[loopImpl](#type_loopImpl "Jump to "loopImpl" type definition.") </[tns](#ns_tns "Find out namespace of 'tns' prefix"):loop> \[0..1\]
      End Choice
   </[tns](#ns_tns "Find out namespace of 'tns' prefix"):sequence>
</...>

#### [Schema Component Representation](#type_loopImpl-schemaComponent-collapse)

<complexType name="loopImpl"\>
   <complexContent\>
      <extension base="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[loopBase](#type_loopBase "Jump to "loopBase" type definition.")"\>
         <sequence\>
            <element name="sequence"\>
               <complexType\>
                  <choice maxOccurs="unbounded"\>
                     <element name="segment" type="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[segmentImpl](#type_segmentImpl "Jump to "segmentImpl" type definition.")"/>
                     <element name="loop" type="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[loopImpl](#type_loopImpl "Jump to "loopImpl" type definition.")" minOccurs="0"/>
                  </choice>
               </complexType>
            </element>
         </sequence>
         <attribute name="type" type="NMTOKEN" use="required"/>
         <attribute name="code" type="NMTOKEN" use="required"/>
         <attribute name="discriminator" type="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[discriminatorType](#type_discriminatorType "Jump to "discriminatorType" type definition.")"/>
      </extension>
   </complexContent>
</complexType>

[](#top "Go to top of page")

* * *

### Complex Type: loopStandard

#### [Type hierarchy](#type_loopStandard-type-hierarchy-collapse)

Super-types:

[baseType](#type_baseType "Jump to "baseType" type definition.") < [loopBase](#type_loopBase "Jump to "loopBase" type definition.") (by extension) < **loopStandard** (by extension)

Sub-types:

None

#### [Properties](#type_loopStandard-properties-table-collapse)

Name

loopStandard

[Abstract](#term_Abstract "Look up 'Abstract' in glossary")

no

#### [Documentation](#type_loopStandard-doc-panel-collapse)

No documentation provided.

#### [XML Instance Representation](#type_loopStandard-instance-table-collapse)

<...
 title="string" \[0..1\]
 minOccurs="nonNegativeInteger" \[0..1\]

×

#### Attribute minOccurs

              The minimum number of times a loop may repeat. A value of 0 (zero)
              indicates that the loop is optional.

              When used in a loop defined
              within an implementation,
              the value may not be less than the value set on the standard loop referenced
              by the implementation loop's 'type'
              attribute.
            

Close

 
 maxOccurs="nonNegativeInteger" \[0..1\]

×

#### Attribute maxOccurs

              The maximum number of times a loop may repeat.
              When used in a loop defined within an implementation, the value
              may not be greater than
              the value set on the standard loop referenced
              by the implementation loop's 'type' attribute.
            

Close

 
 code="NMTOKEN" \[1\]

×

#### Attribute code

              Code used to uniquely identify a loop within the transaction/message.
            

Close

 
\>
   <[tns](#ns_tns "Find out namespace of 'tns' prefix"):[description](#element_description "Jump to "description" element declaration.")\> ... </[tns](#ns_tns "Find out namespace of 'tns' prefix"):[description](#element_description "Jump to "description" element declaration.")\> \[0..1\]
   <[tns](#ns_tns "Find out namespace of 'tns' prefix"):sequence   \> \[1\]  
      Start [Choice](#term_Choice "Look up 'Choice' in glossary") \[1..\*\]
         <[tns](#ns_tns "Find out namespace of 'tns' prefix"):segment> [tns](#ns_tns "Find out namespace of 'tns' prefix"):[segmentStandard](#type_segmentStandard "Jump to "segmentStandard" type definition.") </[tns](#ns_tns "Find out namespace of 'tns' prefix"):segment> \[1\]
         <[tns](#ns_tns "Find out namespace of 'tns' prefix"):loop> [tns](#ns_tns "Find out namespace of 'tns' prefix"):[loopStandard](#type_loopStandard "Jump to "loopStandard" type definition.") </[tns](#ns_tns "Find out namespace of 'tns' prefix"):loop> \[0..1\]
      End Choice
   </[tns](#ns_tns "Find out namespace of 'tns' prefix"):sequence>
   <[tns](#ns_tns "Find out namespace of 'tns' prefix"):[syntax](#element_syntax "Jump to "syntax" element declaration.")\> ... </[tns](#ns_tns "Find out namespace of 'tns' prefix"):[syntax](#element_syntax "Jump to "syntax" element declaration.")\> \[0..\*\]
</...>

#### [Schema Component Representation](#type_loopStandard-schemaComponent-collapse)

<complexType name="loopStandard"\>
   <complexContent\>
      <extension base="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[loopBase](#type_loopBase "Jump to "loopBase" type definition.")"\>
         <sequence\>
            <element name="sequence"\>
               <complexType\>
                  <choice maxOccurs="unbounded"\>
                     <element name="segment" type="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[segmentStandard](#type_segmentStandard "Jump to "segmentStandard" type definition.")"/>
                     <element name="loop" type="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[loopStandard](#type_loopStandard "Jump to "loopStandard" type definition.")" minOccurs="0"/>
                  </choice>
               </complexType>
            </element>
            <element ref="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[syntax](#element_syntax "Jump to "syntax" element declaration.")" minOccurs="0" maxOccurs="unbounded"/>
         </sequence>
         <attribute name="code" type="NMTOKEN" use="required"/>
      </extension>
   </complexContent>
</complexType>

[](#top "Go to top of page")

* * *

### Complex Type: segmentImpl

#### [Type hierarchy](#type_segmentImpl-type-hierarchy-collapse)

Super-types:

[baseType](#type_baseType "Jump to "baseType" type definition.") < **segmentImpl** (by extension)

Sub-types:

None

#### [Properties](#type_segmentImpl-properties-table-collapse)

Name

segmentImpl

[Abstract](#term_Abstract "Look up 'Abstract' in glossary")

no

#### [Documentation](#type_segmentImpl-doc-panel-collapse)

No documentation provided.

#### [XML Instance Representation](#type_segmentImpl-instance-table-collapse)

<...
 title="string" \[0..1\]
 type="NCName" \[1\]

×

#### Attribute type

              The name of the standard segment used at this position in the implementation.
              Must be a valid segment name that occurs in the same
              standard loop.
            

Close

 
 code="NMTOKEN" \[0..1\]

×

#### Attribute code

              Code used to identify a segment within a loop. May be useful when occurrences of a
              standard segment contain distinct information.
            

Close

 
 minOccurs="nonNegativeInteger" \[0..1\]

×

#### Attribute minOccurs

          The minimum number of times a type may occur at the declared location
          in the EDI structure.
        

Close

 
 maxOccurs="nonNegativeInteger" \[0..1\]

×

#### Attribute maxOccurs

          The maximum number of times a type may occur at the declared location
          in the EDI structure.
        

Close

 
 discriminator="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[discriminatorType](#type_discriminatorType "Jump to "discriminatorType" type definition.")" \[0..1\]

×

#### Attribute discriminator

              The element position in the segment used to identify an occurrence
              of a standard segment from other implementation occurrences. The
              element identified by the position given in this attribute must also specify an
              enumeration of values used only by this implementation and not used
              by any other implementations of the standard segment in the same implementation loop.
            

Close

 
\>
   <[tns](#ns_tns "Find out namespace of 'tns' prefix"):[description](#element_description "Jump to "description" element declaration.")\> ... </[tns](#ns_tns "Find out namespace of 'tns' prefix"):[description](#element_description "Jump to "description" element declaration.")\> \[0..1\]
   <[tns](#ns_tns "Find out namespace of 'tns' prefix"):sequence   \> \[0..1\]  
      Start [Choice](#term_Choice "Look up 'Choice' in glossary") \[0..\*\]
         <[tns](#ns_tns "Find out namespace of 'tns' prefix"):element> [tns](#ns_tns "Find out namespace of 'tns' prefix"):[elementImpl](#type_elementImpl "Jump to "elementImpl" type definition.") </[tns](#ns_tns "Find out namespace of 'tns' prefix"):element> \[1\]
         <[tns](#ns_tns "Find out namespace of 'tns' prefix"):composite> [tns](#ns_tns "Find out namespace of 'tns' prefix"):[compositeImpl](#type_compositeImpl "Jump to "compositeImpl" type definition.") </[tns](#ns_tns "Find out namespace of 'tns' prefix"):composite> \[1\]
      End Choice
   </[tns](#ns_tns "Find out namespace of 'tns' prefix"):sequence>
</...>

#### [Schema Component Representation](#type_segmentImpl-schemaComponent-collapse)

<complexType name="segmentImpl"\>
   <complexContent\>
      <extension base="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[baseType](#type_baseType "Jump to "baseType" type definition.")"\>
         <sequence\>
            <element name="sequence" minOccurs="0"\>
               <complexType\>
                  <sequence\>
                     <choice minOccurs="0" maxOccurs="unbounded"\>
                        <element name="element" type="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[elementImpl](#type_elementImpl "Jump to "elementImpl" type definition.")"/>
                        <element name="composite" type="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[compositeImpl](#type_compositeImpl "Jump to "compositeImpl" type definition.")"/>
                     </choice>
                  </sequence>
               </complexType>
            </element>
         </sequence>
         <attribute name="type" type="NCName" use="required"/>
         <attribute name="code" type="NMTOKEN" use="optional"/>
         <attributeGroup ref="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[implementationAttributeGroup](#attributeGroup_implementationAttributeGroup "Jump to "implementationAttributeGroup" attribute group definition.")"/>
         <attribute name="discriminator" type="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[discriminatorType](#type_discriminatorType "Jump to "discriminatorType" type definition.")" use="optional"/>
      </extension>
   </complexContent>
</complexType>

[](#top "Go to top of page")

* * *

### Complex Type: segmentStandard

#### [Type hierarchy](#type_segmentStandard-type-hierarchy-collapse)

Super-types:

[baseType](#type_baseType "Jump to "baseType" type definition.") < **segmentStandard** (by extension)

Sub-types:

None

#### [Properties](#type_segmentStandard-properties-table-collapse)

Name

segmentStandard

[Abstract](#term_Abstract "Look up 'Abstract' in glossary")

no

#### [Documentation](#type_segmentStandard-doc-panel-collapse)

No documentation provided.

#### [XML Instance Representation](#type_segmentStandard-instance-table-collapse)

<...
 title="string" \[0..1\]
 type="NCName" \[0..1\]

×

#### Attribute type

          The name of the target type being referenced.
        

Close

 
 minOccurs="nonNegativeInteger" \[0..1\]

×

#### Attribute minOccurs

          The minimum number of times a type may occur at the declared location
          in the EDI structure.
        

Close

 
 maxOccurs="nonNegativeInteger" \[0..1\]

×

#### Attribute maxOccurs

          The maximum number of times a type may occur at the declared location
          in the EDI structure.
        

Close

 
\>
   <[tns](#ns_tns "Find out namespace of 'tns' prefix"):[description](#element_description "Jump to "description" element declaration.")\> ... </[tns](#ns_tns "Find out namespace of 'tns' prefix"):[description](#element_description "Jump to "description" element declaration.")\> \[0..1\]
</...>

#### [Schema Component Representation](#type_segmentStandard-schemaComponent-collapse)

<complexType name="segmentStandard"\>
   <complexContent\>
      <extension base="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[baseType](#type_baseType "Jump to "baseType" type definition.")"\>
         <attributeGroup ref="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[referenceAttributeGroup](#attributeGroup_referenceAttributeGroup "Jump to "referenceAttributeGroup" attribute group definition.")"/>
      </extension>
   </complexContent>
</complexType>

[](#top "Go to top of page")

* * *

### Complex Type: transactionControlType

#### [Type hierarchy](#type_transactionControlType-type-hierarchy-collapse)

Super-types:

[baseType](#type_baseType "Jump to "baseType" type definition.") < [controlType](#type_controlType "Jump to "controlType" type definition.") (by extension) < **transactionControlType** (by extension)

Sub-types:

None

#### [Properties](#type_transactionControlType-properties-table-collapse)

Name

transactionControlType

[Abstract](#term_Abstract "Look up 'Abstract' in glossary")

no

#### [Documentation](#type_transactionControlType-doc-panel-collapse)

No documentation provided.

#### [XML Instance Representation](#type_transactionControlType-instance-table-collapse)

<...
 title="string" \[0..1\]
 header="NCName" \[1\]
 trailer="NCName" \[1\]
 use="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[useType](#type_useType "Jump to "useType" type definition.")" \[0..1\]
\>
   <[tns](#ns_tns "Find out namespace of 'tns' prefix"):[description](#element_description "Jump to "description" element declaration.")\> ... </[tns](#ns_tns "Find out namespace of 'tns' prefix"):[description](#element_description "Jump to "description" element declaration.")\> \[0..1\]
</...>

#### [Schema Component Representation](#type_transactionControlType-schemaComponent-collapse)

<complexType name="transactionControlType"\>
   <complexContent\>
      <extension base="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[controlType](#type_controlType "Jump to "controlType" type definition.")"\>
         <attribute name="use" type="[tns](#ns_tns "Find out namespace of 'tns' prefix"):[useType](#type_useType "Jump to "useType" type definition.")" default="optional"/>
      </extension>
   </complexContent>
</complexType>

[](#top "Go to top of page")

* * *

### Simple Type: discriminatorType

#### [Type hierarchy](#type_discriminatorType-type-hierarchy-collapse)

Super-types:

decimal < **discriminatorType** (by restriction)

Sub-types:

None

#### [Properties](#type_discriminatorType-properties-table-collapse)

Name

discriminatorType

Content

*   Base XSD Type: decimal

*   _pattern_ = \[0-9\]+(\\.\[0-9\]{1,2}){0,1}
*   1 <= _value_ <= 99.99

#### [Documentation](#type_discriminatorType-doc-panel-collapse)

No documentation provided.

#### [Schema Component Representation](#type_discriminatorType-schemaComponent-collapse)

<simpleType name="discriminatorType"\>
   <restriction base="decimal"\>
      <minInclusive value="1"/>
      <maxInclusive value="99.99"/>
      <pattern value="\[0-9\]+(\\.\[0-9\]{1,2}){0,1}"/>
   </restriction>
</simpleType>

[](#top "Go to top of page")

* * *

### Simple Type: elementBaseType

#### [Type hierarchy](#type_elementBaseType-type-hierarchy-collapse)

Super-types:

string < **elementBaseType** (by restriction)

Sub-types:

None

#### [Properties](#type_elementBaseType-properties-table-collapse)

Name

elementBaseType

Content

*   Base XSD Type: string

*   _value_ comes from list: { 'binary'| 'date'| 'decimal'| 'identifier'| 'numeric'| 'string'| 'time'}

#### [Documentation](#type_elementBaseType-doc-panel-collapse)

No documentation provided.

#### [Schema Component Representation](#type_elementBaseType-schemaComponent-collapse)

<simpleType name="elementBaseType"\>
   <restriction base="string"\>
      <enumeration value="binary"/>
      <enumeration value="date"/>
      <enumeration value="decimal"/>
      <enumeration value="identifier"/>
      <enumeration value="numeric"/>
      <enumeration value="string"/>
      <enumeration value="time"/>
   </restriction>
</simpleType>

[](#top "Go to top of page")

* * *

### Simple Type: nameType

#### [Type hierarchy](#type_nameType-type-hierarchy-collapse)

Super-types:

ID < **nameType** (by restriction)

Sub-types:

None

#### [Properties](#type_nameType-properties-table-collapse)

Name

nameType

Content

*   Base XSD Type: ID

*   _pattern_ = \[A-Z\]\[A-Z0-9\]+

#### [Documentation](#type_nameType-doc-panel-collapse)

No documentation provided.

#### [Schema Component Representation](#type_nameType-schemaComponent-collapse)

<simpleType name="nameType"\>
   <restriction base="ID"\>
      <pattern value="\[A-Z\]\[A-Z0-9\]+"/>
   </restriction>
</simpleType>

[](#top "Go to top of page")

* * *

### Simple Type: positionType

#### [Type hierarchy](#type_positionType-type-hierarchy-collapse)

Super-types:

nonNegativeInteger < **positionType** (by restriction)

Sub-types:

None

#### [Properties](#type_positionType-properties-table-collapse)

Name

positionType

Content

*   Base XSD Type: nonNegativeInteger

*   _value_ >= 1

#### [Documentation](#type_positionType-doc-panel-collapse)

No documentation provided.

#### [Schema Component Representation](#type_positionType-schemaComponent-collapse)

<simpleType name="positionType"\>
   <restriction base="nonNegativeInteger"\>
      <minInclusive value="1"/>
   </restriction>
</simpleType>

[](#top "Go to top of page")

* * *

### Simple Type: syntaxType

#### [Type hierarchy](#type_syntaxType-type-hierarchy-collapse)

Super-types:

string < **syntaxType** (by restriction)

Sub-types:

None

#### [Properties](#type_syntaxType-properties-table-collapse)

Name

syntaxType

Content

*   Base XSD Type: string

*   _value_ comes from list: { 'single'| 'paired'| 'required'| 'exclusion'| 'conditional'| 'list'| 'firstonly'}

#### [Documentation](#type_syntaxType-doc-panel-collapse)

No documentation provided.

#### [Schema Component Representation](#type_syntaxType-schemaComponent-collapse)

<simpleType name="syntaxType"\>
   <restriction base="string"\>
      <enumeration value="single"/>
      <enumeration value="paired"/>
      <enumeration value="required"/>
      <enumeration value="exclusion"/>
      <enumeration value="conditional"/>
      <enumeration value="list"/>
      <enumeration value="firstonly"/>
   </restriction>
</simpleType>

[](#top "Go to top of page")

* * *

### Simple Type: useType

#### [Type hierarchy](#type_useType-type-hierarchy-collapse)

Super-types:

string < **useType** (by restriction)

Sub-types:

None

#### [Properties](#type_useType-properties-table-collapse)

Name

useType

Content

*   Base XSD Type: string

*   _value_ comes from list: {'required'|'optional'|'prohibited'}

#### [Documentation](#type_useType-doc-panel-collapse)

No documentation provided.

#### [Schema Component Representation](#type_useType-schemaComponent-collapse)

<simpleType name="useType"\>
   <restriction base="string"\>
      <enumeration value="required"/>
      <enumeration value="optional"/>
      <enumeration value="prohibited"/>
   </restriction>
</simpleType>

[](#top "Go to top of page")

* * *

Glossary
--------

Abstract (Applies to complex type definitions and element declarations). An abstract element or complex type cannot used to validate an element instance. If there is a reference to an abstract element, only element declarations that can substitute the abstract element can be used to validate the instance. For references to abstract type definitions, only derived types can be used.

All Model Group Child elements can be provided _in any order_ in instances. See: [http://www.w3.org/TR/xmlschema-1/#element-all](http://www.w3.org/TR/xmlschema-1/#element-all "http://www.w3.org/TR/xmlschema-1/#element-all").

Choice Model Group _Only one_ from the list of child elements and model groups can be provided in instances. See: [http://www.w3.org/TR/xmlschema-1/#element-choice](http://www.w3.org/TR/xmlschema-1/#element-choice "http://www.w3.org/TR/xmlschema-1/#element-choice").

Collapse Whitespace Policy Replace tab, line feed, and carriage return characters with space character (Unicode character 32). Then, collapse contiguous sequences of space characters into single space character, and remove leading and trailing space characters.

Disallowed Substitutions (Applies to element declarations). If _substitution_ is specified, then [substitution group](#term_SubGroup "Look up 'substitution group' in glossary") members cannot be used in place of the given element declaration to validate element instances. If _derivation methods_, e.g. extension, restriction, are specified, then the given element declaration will not validate element instances that have types derived from the element declaration's type using the specified derivation methods. Normally, element instances can override their declaration's type by specifying an `xsi:type` attribute.

Key Constraint Like [Uniqueness Constraint](#term_Unique "Look up 'Uniqueness Constraint' in glossary"), but additionally requires that the specified value(s) must be provided. See: [http://www.w3.org/TR/xmlschema-1/#cIdentity-constraint\_Definitions](http://www.w3.org/TR/xmlschema-1/#cIdentity-constraint_Definitions "http://www.w3.org/TR/xmlschema-1/#cIdentity-constraint_Definitions").

Key Reference Constraint Ensures that the specified value(s) must match value(s) from a [Key Constraint](#term_Key "Look up 'Key Constraint' in glossary") or [Uniqueness Constraint](#term_Unique "Look up 'Uniqueness Constraint' in glossary"). See: [http://www.w3.org/TR/xmlschema-1/#cIdentity-constraint\_Definitions](http://www.w3.org/TR/xmlschema-1/#cIdentity-constraint_Definitions "http://www.w3.org/TR/xmlschema-1/#cIdentity-constraint_Definitions").

Model Group Groups together element content, specifying the order in which the element content can occur and the number of times the group of element content may be repeated. See: [http://www.w3.org/TR/xmlschema-1/#Model\_Groups](http://www.w3.org/TR/xmlschema-1/#Model_Groups "http://www.w3.org/TR/xmlschema-1/#Model_Groups").

Nillable (Applies to element declarations). If an element declaration is nillable, instances can use the `xsi:nil` attribute. The `xsi:nil` attribute is the boolean attribute, _nil_, from the _http://www.w3.org/2001/XMLSchema-instance_ namespace. If an element instance has an `xsi:nil` attribute set to true, it can be left empty, even though its element declaration may have required content.

Notation A notation is used to identify the format of a piece of data. Values of elements and attributes that are of type, NOTATION, must come from the names of declared notations. See: [http://www.w3.org/TR/xmlschema-1/#cNotation\_Declarations](http://www.w3.org/TR/xmlschema-1/#cNotation_Declarations "http://www.w3.org/TR/xmlschema-1/#cNotation_Declarations").

Preserve Whitespace Policy Preserve whitespaces exactly as they appear in instances.

Prohibited Derivations (Applies to type definitions). Derivation methods that cannot be used to create sub-types from a given type definition.

Prohibited Substitutions (Applies to complex type definitions). Prevents sub-types that have been derived using the specified derivation methods from validating element instances in place of the given type definition.

Replace Whitespace Policy Replace tab, line feed, and carriage return characters with space character (Unicode character 32).

Sequence Model Group Child elements and model groups must be provided _in the specified order_ in instances. See: [http://www.w3.org/TR/xmlschema-1/#element-sequence](http://www.w3.org/TR/xmlschema-1/#element-sequence "http://www.w3.org/TR/xmlschema-1/#element-sequence").

Substitution Group Elements that are _members_ of a substitution group can be used wherever the _head_ element of the substitution group is referenced.

Substitution Group Exclusions (Applies to element declarations). Prohibits element declarations from nominating themselves as being able to substitute a given element declaration, if they have types that are derived from the original element's type using the specified derivation methods.

Target Namespace The target namespace identifies the namespace that components in this schema belongs to. If no target namespace is provided, then the schema components do not belong to any namespace.

Uniqueness Constraint Ensures uniqueness of an element/attribute value, or a combination of values, within a specified scope. See: [http://www.w3.org/TR/xmlschema-1/#cIdentity-constraint\_Definitions](http://www.w3.org/TR/xmlschema-1/#cIdentity-constraint_Definitions "http://www.w3.org/TR/xmlschema-1/#cIdentity-constraint_Definitions").

[](#top "Go to top of page")

* * *

Generated by [xs3p](https://github.com/Mapudo/xs3p).

$(function () { $("\[data-toggle='tooltip'\]").tooltip(); }); $(function () { $("\[data-toggle='popover'\]").popover(); }); var c = window.markdownit(); $(".xs3p-doc").each(function (i, obj) { var rawDocID = "#" + $(this).attr("id") + "-raw"; var indent = $(rawDocID).html().match("^\\\\n\[\\\\t \]\*"); if (!(indent === null)) { normalized = $(rawDocID) .html() .replace(new RegExp(indent\[0\], "gm"), "\\n"); } else { normalized = $(rawDocID).html(); } $(this).html(c.render(normalized)); $(this) .find("code,pre") .each(function (i, block) { $(this).html($(this).text()); }); }); $(window).scroll(function () { if ( $(".xs3p-sidebar").css("position") == "fixed" && $(window).height() < $(".xs3p-sidebar").height() ) { var perc = $(window).scrollTop() / $("#xs3p-content").height(); var overflow = $(".xs3p-sidebar").height() + 105 - $(window).height(); $(".xs3p-sidebar").css( "top", 65 - Math.round(overflow \* perc) + "px" ); } }); $(window).resize(function () { if ($(".xs3p-sidebar").css("position") == "fixed") { $(".xs3p-sidebar").css("top", "65px"); } });
