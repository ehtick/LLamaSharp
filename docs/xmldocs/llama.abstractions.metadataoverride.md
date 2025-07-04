[`< Back`](./)

---

# MetadataOverride

Namespace: LLama.Abstractions

An override for a single key/value pair in model metadata

```csharp
public sealed class MetadataOverride : System.IEquatable`1[[LLama.Abstractions.MetadataOverride, LLamaSharp, Version=0.0.0.0, Culture=neutral, PublicKeyToken=null]]
```

Inheritance [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) → [MetadataOverride](./llama.abstractions.metadataoverride.md)<br>
Implements [IEquatable&lt;MetadataOverride&gt;](https://docs.microsoft.com/en-us/dotnet/api/system.iequatable-1)<br>
Attributes [NullableContextAttribute](https://docs.microsoft.com/en-us/dotnet/api/system.runtime.compilerservices.nullablecontextattribute), [NullableAttribute](https://docs.microsoft.com/en-us/dotnet/api/system.runtime.compilerservices.nullableattribute), JsonConverterAttribute

## Properties

### **Key**

Get the key being overridden by this override

```csharp
public string Key { get; }
```

#### Property Value

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>

## Constructors

### **MetadataOverride(String, Int32)**

Create a new override for an int key

```csharp
public MetadataOverride(string key, int value)
```

#### Parameters

`key` [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>

`value` [Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)<br>

### **MetadataOverride(String, Single)**

Create a new override for a float key

```csharp
public MetadataOverride(string key, float value)
```

#### Parameters

`key` [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>

`value` [Single](https://docs.microsoft.com/en-us/dotnet/api/system.single)<br>

### **MetadataOverride(String, Boolean)**

Create a new override for a boolean key

```csharp
public MetadataOverride(string key, bool value)
```

#### Parameters

`key` [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>

`value` [Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)<br>

### **MetadataOverride(String, String)**

Create a new override for a string key

```csharp
public MetadataOverride(string key, string value)
```

#### Parameters

`key` [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>

`value` [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>

## Methods

### **ToString()**

```csharp
public string ToString()
```

#### Returns

[String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>

### **GetHashCode()**

```csharp
public int GetHashCode()
```

#### Returns

[Int32](https://docs.microsoft.com/en-us/dotnet/api/system.int32)<br>

### **Equals(Object)**

```csharp
public bool Equals(object obj)
```

#### Parameters

`obj` [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object)<br>

#### Returns

[Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)<br>

### **Equals(MetadataOverride)**

```csharp
public bool Equals(MetadataOverride other)
```

#### Parameters

`other` [MetadataOverride](./llama.abstractions.metadataoverride.md)<br>

#### Returns

[Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)<br>

### **&lt;Clone&gt;$()**

```csharp
public MetadataOverride <Clone>$()
```

#### Returns

[MetadataOverride](./llama.abstractions.metadataoverride.md)<br>

---

[`< Back`](./)
