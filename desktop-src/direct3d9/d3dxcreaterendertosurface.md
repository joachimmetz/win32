---
Description: Creates a render surface.
ms.assetid: 35e0007e-c405-46e1-a52b-625adc84732b
title: D3DXCreateRenderToSurface function
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# D3DXCreateRenderToSurface function

Creates a render surface.

## Syntax


```C++
HRESULT D3DXCreateRenderToSurface(
  _In_  LPDIRECT3DDEVICE9     pDevice,
  _In_  UINT                  Width,
  _In_  UINT                  Height,
  _In_  D3DFORMAT             Format,
  _In_  BOOL                  DepthStencil,
  _In_  D3DFORMAT             DepthStencilFormat,
  _Out_ LPD3DXRENDERTOSURFACE *ppRenderToSurface
);
```



## Parameters

<dl> <dt>

*pDevice* \[in\]
</dt> <dd>

Type: **[**LPDIRECT3DDEVICE9**](/windows/desktop/api/d3d9helper/nn-d3d9-idirect3ddevice9)**

Pointer to an [**IDirect3DDevice9**](/windows/desktop/api/d3d9helper/nn-d3d9-idirect3ddevice9) interface, the device to be associated with the render surface.

</dd> <dt>

*Width* \[in\]
</dt> <dd>

Type: **[**UINT**](https://msdn.microsoft.com/windows/desktop/4553cafc-450e-4493-a4d4-cb6e2f274d46)**

Width of the render surface, in pixels.

</dd> <dt>

*Height* \[in\]
</dt> <dd>

Type: **[**UINT**](https://msdn.microsoft.com/windows/desktop/4553cafc-450e-4493-a4d4-cb6e2f274d46)**

Height of the render surface, in pixels.

</dd> <dt>

*Format* \[in\]
</dt> <dd>

Type: **[D3DFORMAT](d3dformat.md)**

Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the pixel format of the render surface.

</dd> <dt>

*DepthStencil* \[in\]
</dt> <dd>

Type: **[**BOOL**](https://msdn.microsoft.com/windows/desktop/4553cafc-450e-4493-a4d4-cb6e2f274d46)**

If **TRUE**, the render surface supports a depth-stencil surface. Otherwise, this member is set to **FALSE**. This function will create a new depth buffer.

</dd> <dt>

*DepthStencilFormat* \[in\]
</dt> <dd>

Type: **[D3DFORMAT](d3dformat.md)**

If *DepthStencil* is set to **TRUE**, this parameter is a member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the depth-stencil format of the render surface.

</dd> <dt>

*ppRenderToSurface* \[out\]
</dt> <dd>

Type: **[**LPD3DXRENDERTOSURFACE**](id3dxrendertosurface.md)\***

Address of a pointer to an [**ID3DXRenderToSurface**](id3dxrendertosurface.md) interface, representing the created render surface.

</dd> </dl>

## Return value

Type: **[**HRESULT**](https://msdn.microsoft.com/windows/desktop/455d07e9-52c3-4efb-a9dc-2955cbfd38cc)**

If the function succeeds, the return value is D3D\_OK. If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.

## Requirements



|                    |                                                                                        |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Library<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## See also

<dl> <dt>

[General Purpose Functions](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 



