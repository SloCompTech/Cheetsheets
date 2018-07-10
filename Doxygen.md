Short docs from [Doxygen](https://www.stack.nl/~dimitri/doxygen/manual/install.html)

## Blocks
|**Block name**|**Description**|
|:------------:|:--------------|
|`@brief description`|Brief description|
|`@file <filename>`|File name|
|`@def <define>`|Define|
|`@struct <name>`|Struct|
|`@warning <warning>`|Warning|
|`@var <name>`|Define, variable, typedef|
|`@class <name>`|Class|
|`@see <ref>`|Reference|
|`@param {[in]|[out]|[in,out]} <name> <desc>`|Function parameter|
|`@return <desc>`|Return of function|
|`@deprecated <desc>`|Deprecated|
|`@bug <desc>`|Bug description|
|`@author <author>`|Author, can be multiple times|
|`@authors <authors list>`|Authors|
|`@attention <text>`|Attention|
|`@throw <exception> <desc>`|Throw exception|
|`@todo <paragraph>`|TODO paragraph|
|`@version <version>`|Version|
|`@note <note>`|Note|
|`@parblock`|Multi block param,warning,note description|
|`@endparblock`|End of parblock|


### File
```c++
/**
*   @file filename.h
*   @brief <brief>
*   
*   <details>
*/
```

### Define
```c++
/*
*   @brief <brief>
*
*   <details>
*/
```

### Typedef
```c++
/**
*   @brief <bried>
*
*   <details>
*/
typedef unsigned int teto;
```

### Comment block
```c++
/**
 * ... text ...
 */
```

### Struct
```c++
/**
*   @brief <brief>
*
*   <details>
*/
struct SName {

};
```

### Variables
```c++
int var; ///< Detailed description after the member
```

### Group
```c++
/**
*   @addtogroup <name>
*  @{
*/

///@}
```
### Link to web page or URL
```c++
/**
*   <a href="www.example.com">My link</a>
*/
```

### Links classes
```c++
/**
*   Word with at least one non-lowercase
*   %prevent link
*   @ref manualclass
*/
```

### Links to files
```c++
/**
* File.h (. in word not at the end or begining)
*/
```

### Links to functions
```c++
/**
*   <functionName>"("<argument-list>")"
*   <functionName>"()"
*   "::"<functionName>
*   (<className>"::")n<functionName>"("<argument-list>")"
*   (<className>"::")n<functionName>"("<argument-list>")"<modifiers>
*   (<className>"::")n<functionName>"()"
*   (<className>"::")n<functionName>
*
*/
```

### Links to members
```c++
/*! \file autolink.cpp
  Testing automatic link generation.
  
  

  A link to a member of the Autolink_Test class: Autolink_Test::member, 
  
  More specific links to the each of the overloaded members:
  Autolink_Test::member(int) and Autolink_Test#member(int,int)
  A link to a protected member variable of Autolink_Test: Autolink_Test#var, 
  A link to the global enumeration type #GlobEnum.
 
  A link to the define #ABS(x).
  
  A link to the destructor of the Autolink_Test class: Autolink_Test::~Autolink_Test, 
  
  A link to the typedef ::B.
 
  A link to the enumeration type Autolink_Test::EType
  
  A link to some enumeration values Autolink_Test::Val1 and ::GVal2
*/
/*!
  Since this documentation block belongs to the class Autolink_Test no link to 
  Autolink_Test is generated.
  Two ways to link to a constructor are: #Autolink_Test and Autolink_Test().
  Links to the destructor are: #~Autolink_Test and ~Autolink_Test().
  
  A link to a member in this class: member().
  More specific links to the each of the overloaded members: 
  member(int) and member(int,int). 
  
  A link to the variable #var.
  A link to the global typedef ::B.
  A link to the global enumeration type #GlobEnum.
  
  A link to the define ABS(x).
  
  A link to a variable \link #var using another text\endlink as a link.
  
  A link to the enumeration type #EType.
  A link to some enumeration values: \link Autolink_Test::Val1 Val1 \endlink and ::GVal1.
  And last but not least a link to a file: autolink.cpp.
  
  \sa Inside a see also section any word is checked, so EType, 
      Val1, GVal1, ~Autolink_Test and member will be replaced by links in HTML.
*/

```