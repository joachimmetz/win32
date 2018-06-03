---
Description: Returns the name of the highest high-level shader language (HLSL) profile supported by a given device.
ms.assetid: a50e2a17-8170-4364-a562-7886593341b3
title: D3DXGetVertexShaderProfile function
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# D3DXGetVertexShaderProfile function

Returns the name of the highest high-level shader language (HLSL) profile supported by a given device.

## Syntax


```C++
LPCSTR D3DXGetVertexShaderProfile(
  _In_ LPDIRECT3DDEVICE9 pDevice
);
```



## Parameters

<dl> <dt>

*pDevice* \[in\]
</dt> <dd>

Type: **[**LPDIRECT3DDEVICE9**](/windows/desktop/api/d3d9helper/nn-d3d9-idirect3ddevice9)**

Pointer to the device. See [**IDirect3DDevice9**](/windows/desktop/api/d3d9helper/nn-d3d9-idirect3ddevice9).

</dd> </dl>

## Return value

Type: **[**LPCSTR**](https://msdn.microsoft.com/windows/desktop/4553cafc-450e-4493-a4d4-cb6e2f274d46)**

The HLSL profile name.

If the device does not support vertex shaders then the function returns **NULL**.

## Remarks

A shader profile specifies the assembly shader version to use and the capabilities available to the HLSL compiler when compiling a shader. The following table lists the vertex shader profiles that are supported.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Shader Profile</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>vs_1_1</td>
<td>Compile to vs_1_1 version.</td>
</tr>
<tr class="even">
<td>vs_2_0</td>
<td>Compile to vs_2_0 version.</td>
</tr>
<tr class="odd">
<td>vs_2_a</td>
<td>Same as the vs_2_0 profile, with the following additional capabilities available for the compiler to target:
<ul>
<li>Number of Temporary Registers (r#) is greater than or equal to 13.</li>
<li>Dynamic flow control instruction.</li>
<li>Predication.</li>
</ul></td>
</tr>
<tr class="even">
<td>vs_3_0</td>
<td>Compile to vs_3_0 version.</td>
</tr>
</tbody>
</table>



 

For more information about the differences between shader versions, see [Vertex Shader Differences](https://msdn.microsoft.com/windows/desktop/94fe4033-94c0-4561-b0fd-1fb85d8f796b).

## Requirements



|                    |                                                                                          |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Library<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## See also

<dl> <dt>

[Shader Functions](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 



