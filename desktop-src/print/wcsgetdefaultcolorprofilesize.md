---
Description: The WcsGetDefaultColorProfileSize function returns the size, in bytes, of the default color profile name for a device, including the NULL terminator.
ms.assetid: d04306e2-3479-4ba4-ac4d-bf3715487fcf
title: WcsGetDefaultColorProfileSize function
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# WcsGetDefaultColorProfileSize function

The `WcsGetDefaultColorProfileSize` function returns the size, in bytes, of the default color profile name for a device, including the **NULL** terminator.

## Syntax


```C++
BOOL WcsGetDefaultColorProfileSize(
  _In_     WCS_PROFILE_MANAGEMENT_SCOPE profileManagementScope,
  _In_opt_ PCWSTR                       pDeviceName,
  _In_     COLORPROFILETYPE             cptColorProfileType,
  _In_     COLORPROFILESUBTYPE          cpstColorProfileSubType,
  _In_     DWORD                        dwProfileID,
  _Out_    PDWORD                       pcbProfileName
);
```



## Parameters

<dl> <dt>

*profileManagementScope* \[in\]
</dt> <dd>

A [**WCS\_PROFILE\_MANAGEMENT\_SCOPE**](wcs-profile-management-scope.md) value that specifies the scope of this profile management operation.

</dd> <dt>

*pDeviceName* \[in, optional\]
</dt> <dd>

A pointer to the name of the device for which the default color profile is to be obtained. If **NULL**, a device-independent default profile will be used.

</dd> <dt>

*cptColorProfileType* \[in\]
</dt> <dd>

A [**COLORPROFILETYPE**](colorprofiletype.md) value that specifies the color profile type.

</dd> <dt>

*cpstColorProfileSubType* \[in\]
</dt> <dd>

A [**COLORPROFILESUBTYPE**](colorprofilesubtype.md) value that specifies the color profile subtype.

</dd> <dt>

*dwProfileID* \[in\]
</dt> <dd>

The ID of the color space that the color profile represents.

</dd> <dt>

*pcbProfileName* \[out\]
</dt> <dd>

A pointer to a location that receives the size, in bytes, of the path name of the default color profile, including the null terminator.

</dd> </dl>

## 

If this function succeeds, the return value is **TRUE**.

If this function fails, the return value is **FALSE**. For extended error information, call **GetLastError** (described in the Microsoft Windows SDK documentation).

## Remarks

Use this function to return the required size of the buffer pointed to by the *pProfileName* parameter in the [**WcsGetDefaultColorProfile**](wcsgetdefaultcolorprofile.md) function.

This function is executable in Least-Privileged User Account (LUA) context.

## Requirements



|                            |                                                                                                                                         |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| Target platform<br/> | <dl> <dt>[Universal](http://go.microsoft.com/fwlink/p/?linkid=531356)</dt> </dl> |
| Version<br/>         | Included in Windows Vista and later.<br/>                                                                                         |
| Header<br/>          | <dl> <dt>Icm.h</dt> </dl>                                                        |
| Library<br/>         | <dl> <dt>Mscms.lib</dt> </dl>                                                    |
| DLL<br/>             | <dl> <dt>Mscms.dll</dt> </dl>                                                    |



## See also

<dl> <dt>

[**COLORPROFILESUBTYPE**](colorprofilesubtype.md)
</dt> <dt>

[**COLORPROFILETYPE**](colorprofiletype.md)
</dt> <dt>

[**WCS\_PROFILE\_MANAGEMENT\_SCOPE**](wcs-profile-management-scope.md)
</dt> <dt>

[**WcsGetDefaultColorProfile**](wcsgetdefaultcolorprofile.md)
</dt> </dl>

 

 

[Send comments about this topic to Microsoft](mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback%20%5Bprint\print%5D:%20WcsGetDefaultColorProfileSize%20function%20%20RELEASE:%20%285/12/2018%29&body=%0A%0APRIVACY%20STATEMENT%0A%0AWe%20use%20your%20feedback%20to%20improve%20the%20documentation.%20We%20don't%20use%20your%20email%20address%20for%20any%20other%20purpose,%20and%20we'll%20remove%20your%20email%20address%20from%20our%20system%20after%20the%20issue%20that%20you're%20reporting%20is%20fixed.%20While%20we're%20working%20to%20fix%20this%20issue,%20we%20might%20send%20you%20an%20email%20message%20to%20ask%20for%20more%20info.%20Later,%20we%20might%20also%20send%20you%20an%20email%20message%20to%20let%20you%20know%20that%20we've%20addressed%20your%20feedback.%0A%0AFor%20more%20info%20about%20Microsoft's%20privacy%20policy,%20see%20http://privacy.microsoft.com/en-us/default.aspx. "Send comments about this topic to Microsoft")




