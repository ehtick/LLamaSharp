[`< Back`](./)

---

# InteractiveExecutor

Namespace: LLama

The LLama executor for interactive mode.

```csharp
public class InteractiveExecutor : StatefulExecutorBase, LLama.Abstractions.ILLamaExecutor
```

Inheritance [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) → [StatefulExecutorBase](./llama.statefulexecutorbase.md) → [InteractiveExecutor](./llama.interactiveexecutor.md)<br>
Implements [ILLamaExecutor](./llama.abstractions.illamaexecutor.md)<br>
Attributes [NullableContextAttribute](https://docs.microsoft.com/en-us/dotnet/api/system.runtime.compilerservices.nullablecontextattribute), [NullableAttribute](https://docs.microsoft.com/en-us/dotnet/api/system.runtime.compilerservices.nullableattribute)

## Fields

### **_logger**

The logger used by this executor.

```csharp
protected ILogger _logger;
```

### **_pastTokensCount**

The tokens that were already processed by the model.

```csharp
protected int _pastTokensCount;
```

### **_consumedTokensCount**

The tokens that were consumed by the model during the current inference.

```csharp
protected int _consumedTokensCount;
```

### **_n_session_consumed**



```csharp
protected int _n_session_consumed;
```

### **_n_matching_session_tokens**



```csharp
protected int _n_matching_session_tokens;
```

### **_pathSession**

The path of the session file.

```csharp
protected string _pathSession;
```

### **_embeds**

A container of the tokens to be processed and after processed.

```csharp
protected List<LLamaToken> _embeds;
```

### **_embed_inps**

A container for the tokens of input.

```csharp
protected List<LLamaToken> _embed_inps;
```

### **_session_tokens**



```csharp
protected List<LLamaToken> _session_tokens;
```

### **_last_n_tokens**

The last tokens generated by the model.

```csharp
protected FixedSizeQueue<LLamaToken> _last_n_tokens;
```

## Properties

### **Context**

The context used by the executor.

```csharp
public LLamaContext Context { get; }
```

#### Property Value

[LLamaContext](./llama.llamacontext.md)<br>

### **IsMultiModal**

```csharp
public bool IsMultiModal { get; }
```

#### Property Value

[Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)<br>

### **ClipModel**

```csharp
public LLavaWeights ClipModel { get; }
```

#### Property Value

[LLavaWeights](./llama.llavaweights.md)<br>

### **Images**

```csharp
public List<Byte[]> Images { get; }
```

#### Property Value

[List&lt;Byte[]&gt;](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.list-1)<br>

## Constructors

### **InteractiveExecutor(LLamaContext, ILogger)**



```csharp
public InteractiveExecutor(LLamaContext context, ILogger logger)
```

#### Parameters

`context` [LLamaContext](./llama.llamacontext.md)<br>

`logger` ILogger<br>

### **InteractiveExecutor(LLamaContext, LLavaWeights, ILogger)**



```csharp
public InteractiveExecutor(LLamaContext context, LLavaWeights clipModel, ILogger logger)
```

#### Parameters

`context` [LLamaContext](./llama.llamacontext.md)<br>

`clipModel` [LLavaWeights](./llama.llavaweights.md)<br>

`logger` ILogger<br>

## Methods

### **GetStateData()**

```csharp
public ExecutorBaseState GetStateData()
```

#### Returns

[ExecutorBaseState](./llama.statefulexecutorbase.executorbasestate.md)<br>

### **LoadState(ExecutorBaseState)**

```csharp
public Task LoadState(ExecutorBaseState data)
```

#### Parameters

`data` [ExecutorBaseState](./llama.statefulexecutorbase.executorbasestate.md)<br>

#### Returns

[Task](https://docs.microsoft.com/en-us/dotnet/api/system.threading.tasks.task)<br>

### **SaveState(String)**

```csharp
public Task SaveState(string filename)
```

#### Parameters

`filename` [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>

#### Returns

[Task](https://docs.microsoft.com/en-us/dotnet/api/system.threading.tasks.task)<br>

### **LoadState(String)**

```csharp
public Task LoadState(string filename)
```

#### Parameters

`filename` [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>

#### Returns

[Task](https://docs.microsoft.com/en-us/dotnet/api/system.threading.tasks.task)<br>

### **GetLoopCondition(InferStateArgs)**

Define whether to continue the loop to generate responses.

```csharp
protected Task<bool> GetLoopCondition(InferStateArgs args)
```

#### Parameters

`args` [InferStateArgs](./llama.statefulexecutorbase.inferstateargs.md)<br>

#### Returns

[Task&lt;Boolean&gt;](https://docs.microsoft.com/en-us/dotnet/api/system.threading.tasks.task-1)<br>

### **PreprocessInputs(String, InferStateArgs)**

```csharp
protected Task PreprocessInputs(string text, InferStateArgs args)
```

#### Parameters

`text` [String](https://docs.microsoft.com/en-us/dotnet/api/system.string)<br>

`args` [InferStateArgs](./llama.statefulexecutorbase.inferstateargs.md)<br>

#### Returns

[Task](https://docs.microsoft.com/en-us/dotnet/api/system.threading.tasks.task)<br>

### **PostProcess(IInferenceParams, InferStateArgs)**

Return whether to break the generation.

```csharp
protected Task<ValueTuple<bool, IReadOnlyList<string>>> PostProcess(IInferenceParams inferenceParams, InferStateArgs args)
```

#### Parameters

`inferenceParams` [IInferenceParams](./llama.abstractions.iinferenceparams.md)<br>

`args` [InferStateArgs](./llama.statefulexecutorbase.inferstateargs.md)<br>

#### Returns

[Task&lt;ValueTuple&lt;Boolean, IReadOnlyList&lt;String&gt;&gt;&gt;](https://docs.microsoft.com/en-us/dotnet/api/system.threading.tasks.task-1)<br>

### **InferInternal(IInferenceParams, InferStateArgs)**

```csharp
protected Task InferInternal(IInferenceParams inferenceParams, InferStateArgs args)
```

#### Parameters

`inferenceParams` [IInferenceParams](./llama.abstractions.iinferenceparams.md)<br>

`args` [InferStateArgs](./llama.statefulexecutorbase.inferstateargs.md)<br>

#### Returns

[Task](https://docs.microsoft.com/en-us/dotnet/api/system.threading.tasks.task)<br>

---

[`< Back`](./)
