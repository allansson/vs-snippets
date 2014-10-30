# Description

This repository contains a collection of some of my most frequently used Visual Studio-snippets.

# Snippets

## confp

Quickly sets up a configuration property, which comes in handy when writing your own configuration section code.

### Properties

* type - The type of the configuration property. Will be used for casting to and from the base-class.
* name - Name of the C#-property.
* xmlname - Name of the XML-element in the applications configuration file.

### Example Output

``` C#
private const string MaxRequestsXmlElementName = "maxRequests";

[ConfigurationProperty(MaxRequestsXmlElementName)]
public int MaxRequests
{
	get 
	{
		return (int)base[MaxRequestsXmlElementName];
	}
	set
	{
		base[MaxRequestsXmlElementName] = value;
	}
}
```

## datac

Creates a DataContract-class. Usable when fiddling about alot with WCF-services and the DataContractSerializer.

### Properties

* name - Name of the DataContract-class.

### Example Output

``` C#
[DataContract]
public class MyDataContract
{

}
```

## datam

Creates a DataMember-property. Usable when fiddling about alot with WCF-services and the DataContractSerializer.

### Properties

* type - The type of the DataMember-property
* name - The name of the DataMember-property

### Example Output

``` C#
[DataMember]
public string CustomerName { get; set; }
```

# License

Seriously? Do I need one? Just do whatever you like with it. :)