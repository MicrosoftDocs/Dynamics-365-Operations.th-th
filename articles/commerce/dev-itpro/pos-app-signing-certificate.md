---
title: ลงชื่อไฟล์ MPOS .appx ด้วยใบรับรองการลงชื่อโค้ด
description: บทความนี้อธิบายวิธีการลงชื่อ MPOS ด้วยใบรับรองการเซ็นโค้ด
author: mugunthanm
ms.date: 05/27/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: tfehr
ms.custom: 28021
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2019-09-2019
ms.openlocfilehash: 7e998514081cad1c7302aacb1cd74373f896f2d0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8865980"
---
# <a name="sign-the-mpos-appx-file-with-a-code-signing-certificate"></a>ลงชื่อไฟล์ MPOS .appx ด้วยใบรับรองการลงชื่อโค้ด

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

เมื่อต้องการติดตั้ง Modern POS (MPOS) คุณต้องลงชื่อแอป MPOS ด้วยใบรับรองการเซ็นโค้ดจากผู้ให้บริการที่เชื่อถือได้และติดตั้งใบรับรองเดียวกันบนเครื่องทั้งหมดที่ MPOS ติดตั้งภายใต้โฟลเดอร์รากที่เชื่อถือได้ของผู้ใช้ปัจจุบัน

เมื่อต้องการลงชื่อแอป MPOS ด้วยใบรับรอง ให้ใช้ตัวเลือกใดตัวเลือกหนึ่งต่อไปนี้ในไฟล์ **Retail SDK\\Build tool\\Customization.settings**:

- เพิ่มส่วนงาน Secure File ของขั้นตอนการสร้างของ Azure DevOps และอัปโหลดใบรับรองเพื่อทำงานทำให้ไฟล์ปลอดภัย ใช้ตัวแปรพาธเอาต์พุตของงาน Secure File เป็นพารามิเตอร์ในไฟล์ Customization.settings

    > [!NOTE]
    > งาน Secure File ไม่รองรับใบรับรองที่มีการป้องกันด้วยรหัสผ่าน คุณต้องเอารหัสผ่านออกก่อนอัปโหลดงานนี้ เนื่องจากใบรับรองถูกอัปโหลดไปยังงานของระบบไฟล์ที่ปลอดภัยใน Azure ดังนั้นคุณสามารถเอารหัสผ่านออกในขั้นตอนนี้เท่านั้น อย่างไรก็ตาม คุณควรหารือเกี่ยวกับการเอารหัสผ่านออกกับผู้เชี่ยวชาญด้านความปลอดภัยเพื่อพิจารณาว่านี่เป็นการดำเนินการที่ถูกต้องสำหรับโครงการของคุณหรือไม่ อย่าเอารหัสผ่านใบรับรองของสถานการณ์อื่นๆ ออก
- ใช้ใบรับรองในระบบไฟล์ โดยให้ดาวน์โหลดหรือสร้างใบรับรองและวางในระบบไฟล์ที่การสร้างยังทำงานอยู่ ผู้ใช้เอเจนต์หรือบิลด์ที่โฮสต์ Microsoft ควรมีสิทธิ์เข้าถึงพาธและไฟล์นี้
- ใช้รหัสประจำตัวเพื่อค้นหาในใบรับรองในที่เก็บและลงชื่อเข้าใช้ด้วยใบรับรองนั้น

## <a name="use-a-secure-file-task-for-universal-windows-platform-app-signing"></a>ใช้งาน Secure File เพื่อลงชื่อแอป Universal Windows Platform

> [!NOTE]
> คุณยังสามารถใช้ Azure Key Vault เพื่อจัดเก็บใบรับรองและใช้เครื่องมือลงชื่อ Azure เพื่อลงชื่อไฟล์ .appx ของ Modern POS และตัวติดตั้งระบบบริการตนเอง สำหรับสคริปต์ไปป์ไลน์ตัวอย่างและข้อมูลเพิ่มเติม โปรดดู [ตั้งค่าไปป์ไลน์การสร้างใน Azure DevOps เพื่อสร้างแพคเกจระบบบริการตนเองของ Retail](build-pipeline.md#set-up-a-build-pipeline-in-azure-devops-to-generate-retail-self-service-packages)

การใช้งาน Secure File เป็นแนวทางที่แนะนำสำหรับการลงชื่อแอป Universal Windows Platform (UWP) สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการลงชื่อแพคเกจ โปรดดู [ตั้งค่าคอนฟิกการลงชื่อแพคเกจ](/windows/uwp/packaging/auto-build-package-uwp-apps#configure-package-signing) กระบวนการนี้จะแสดงในรูปภาพต่อไปนี้

![ขั้นตอนการลงชื่อแอป MPOS](media/POSSigningFlow.png)

> [!NOTE]
> ปัจจุบันการจัดทำแพคเกจ OOB รองรับการลงชื่อเฉพาะไฟล์ .appx เท่านั้น ตัวติดตั้งระบบบริการตนเองต่างๆ เช่น MP CSV, DLL และ HWS ไม่ได้ลงชื่อโดยกระบวนการนี้ คุณต้องลงชื่อด้วยตนเองโดยใช้ SignTool หรือเครื่องมือการลงชื่ออื่นๆ คุณต้องติดตั้งใบรับรองที่ใช้เพื่อลงชื่อไฟล์ .appx ในเครื่องที่ติดตั้ง Modern POS

## <a name="steps-to-configure-the-certificate-for-signing-in-azure-pipelines"></a>ขั้นตอนในการตั้งค่าคอนฟิกใบรับรองการลงชื่อในไปป์ไลน์ Azure

### <a name="certificate-in-the-file-systemsecure-location"></a>ใบรับรองในระบบไฟล์/ตำแหน่งที่ตั้งที่ปลอดภัย

ดาวน์โหลด [งาน DownloadFile](/visualstudio/msbuild/downloadfile-task) และเพิ่มเป็นขั้นตอนแรกในกระบวนการสร้าง ประโยชน์ของการใช้งาน Secure File คือไฟล์จะถูกเข้ารหัสและวางในดิสก์ในระหว่างการสร้าง ไม่ว่าไปป์ไลน์การสร้างจะประสบความสเร็จ ล้มเหลว หรือถูกยกเลิก ไฟล์จะถูกลบออกจากที่ตั้งในการดาวน์โหลดหลังจากกระบวนการสร้างเสร็จสมบูรณ์

1. ดาวน์โหลดและเพิ่มงาน Secure File เป็นขั้นตอนแรกในไปป์ไลน์การสร้างของ Azure คุณสามารถดาวน์โหลดงาน Secure File ได้จาก [DownloadFile](https://marketplace.visualstudio.com/items?itemName=automagically.DownloadFile)
1. อัปโหลดใบรับรองไปยังงาน Secure File และตั้งค่าชื่อการอ้างอิงภายใต้ตัวแปรเอาต์พุต ดังที่แสดงในรูปภาพต่อไปนี้
    > [!div class="mx-imgBorder"]
    > ![งาน Secure File](media/SecureFile.png)
1. สร้างตัวแปรใหม่ในไปป์ไลน์ Azure โดยเลือก **ตัวแปรใหม่** ภายใต้แท็บ **ตัวแปร**
1. ระบุชื่อให้กับตัวแปรในฟิลด์ค่า ตัวอย่างเช่น **MySigningCert**
1. บันทึกตัวแปร
1. เปิดไฟล์ **Customization.settings** จาก **RetailSDK\\BuildTools** และอัปเดต **ModernPOSPackageCertificateKeyFile** ด้วยชื่อตัวแปรที่สร้างในไปป์ไลน์ (ขั้นตอน 3) ตัวอย่างเช่น:

    ```Xml
    <ModernPOSPackageCertificateKeyFile Condition="'$(ModernPOSPackageCertificateKeyFile)' ==''">$(MySigningCert)</ModernPOSPackageCertificateKeyFile>
    ```
    ขั้นตอนนี้ต้องใช้เมื่อใบรับรองไม่ได้รับการป้องกันด้วยรหัสผ่าน หากใบรับรองมีการป้องกันด้วยรหัสผ่าน ให้ปฏิบัติตามขั้นตอนต่อไปนี้
    
1. ถ้าคุณต้องการประทับเวลาไฟล์ .appx ของ MPOS เมื่อลงชื่อพร้อมใบรับรอง ให้เปิดไฟล์ **Retail SDK\\Build tool\\Customization.settings** และอัปเดตตัวแปร **ModernPOSPackageCertificateTimestamp** ด้วยตัวให้บริการประทับเวลา (ตัวอย่างเช่น `http://timestamp.digicert.com`)
1. บนแท็บ **ตัวแปร** ของไปป์ไลน์ ให้เพิ่มตัวแปรข้อความที่ปลอดภัยใหม่ ตั้งชื่อเป็น **MySigningCert.secret** และตั้งค่าของรหัสผ่านเป็นใบรับรอง เลือกไอคอนล็อกเพื่อรักษาความปลอดภัยตัวแปร
1. เพิ่มงาน **Powershell Script** ลงในไปป์ไลน์ (หลังจากดาวน์โหลด Secure File และก่อนขั้นตอนการสร้าง) ระบุชื่อ **การแสดงผล** และตั้งค่าเป็น **Inline** คัดลอกและวางรายการต่อไปนี้ลงในส่วนสคริปต์

    ```powershell
    Write-Host "Start adding the PFX file to the certificate store."
    $pfxpath = '$(MySigningCert.secureFilePath)'
    $secureString = ConvertTo-SecureString "$(MySigningCert.secret)" -AsPlainText -Force
    Import-PfxCertificate -FilePath $pfxpath -CertStoreLocation Cert:\CurrentUser\My -Password $secureString
    ```

1. เปิดไฟล์ **Customization.settings** จาก **RetailSDK\\BuildTools** และอัปเดต **ModernPOSPackageCertificateThumbprint** ด้วยค่ารหัสประจำตัวของใบรับรอง

    ```Xml
       <ModernPOSPackageCertificateThumbprint Condition="'$(ModernPOSPackageCertificateThumbprint)' == ''"></ModernPOSPackageCertificateThumbprint>
    ```
 
สำหรับรายละเอียดเกี่ยวกับวิธีรับรหัสประจำตัวสำหรับใบรับรอง โปรดดู [เรียกดูรหัสประจำตัวของใบรับรอง](/dotnet/framework/wcf/feature-details/how-to-retrieve-the-thumbprint-of-a-certificate#to-retrieve-a-certificates-thumbprint) 

## <a name="download-or-generate-a-certificate-to-sign-the-mpos-app-manually-using-msbuild-in-sdk"></a>ดาวน์โหลดหรือสร้างใบรับรองเพื่อลงชื่อแอป MPOS ด้วยตนเองโดยใช้ msbuild ใน SDK

หากใบรับรองที่ดาวน์โหลดหรือสร้างมีการใช้เพื่อลงชื่อแอป MPOS ให้อัปเดตโหนด **ModernPOSPackageCertificateKeyFile** ในไฟล์ **BuildTools\\Customization.settings** เพื่อชี้ไปยังตำแหน่งไฟล์ pfx (**$(SdkReferencesPath)\\appxsignkey.pfx**) ตัวอย่างเช่น:

```xml
<ModernPOSPackageCertificateKeyFile Condition="'$(ModernPOSPackageCertificateKeyFile)' ==''">$(SdkReferencesPath)\appxsignkey.pfx</ModernPOSPackageCertificateKeyFile>
```

ในกรณีนี้ ชื่อไฟล์ใบรับรองคือ **appxsignkey.pfx** ซึ่งอยู่ในโฟลเดอร์ **Retail SDK\\Reference**

## <a name="use-thumbprint-to-sign-the-mpos-app"></a>ใช้รหัสประจำตัวเพื่อลงชื่อแอป MPOS

ถ้าคุณใช้รหัสประจำตัวเพื่อลงชื่อแอป MPOS ให้ติดตั้งใบรับรองภายในเครื่อง อัปเดตค่ารหัสประจำตัวในโหนด **ModernPOSPackageCertificateThumbprint** ในไฟล์ **BuildTools\\Customization.settings**

ตัวเลือกนี้จะทำงานถ้าผู้ใช้การสร้างเป็นผู้ใช้ภายในเครื่อง อย่างไรก็ตาม ถ้าคุณใช้เอเจนต์ Azure DevOps ในการสร้างบิลด์ เอเจนต์ตัวแทนอาจไม่มีสิทธิ์ในการเข้าถึงที่เก็บใบรับรองเพื่อใช้ใบรับรองในการลงชื่อหรือเครื่องบิลด์จะไม่ได้ติดตั้งใบรับรอง ในกรณีนี้ วิธีแก้ไขคือการเปลี่ยนผู้ใช้บิลด์เป็นผู้ใช้ภายในเครื่องและติดตั้งใบรับรองในกล่อง อย่างไรก็ตาม ตัวเลือกนี้จะใช้ไม่ได้หากคุณไม่มีสิทธิ์ของผู้ดูแลระบบในการเข้าถึงกล่อง

> [!NOTE]
> หากมีการใช้ไฟล์ .pfx หรือตัวเลือกงาน Secure File เพื่อลงชื่อแอป ให้ปล่อยโหนด **ModernPOSPackageCertificateThumbprint** ใน **Customization.settings** เว้นว่างไว้ หากมีการใช้ตัวเลือกรหัสประจำตัว ให้ปล่อย **ModernPOSPackageCertificateKeyFile** เว้นว่างไว้ ถ้ามีการอัปเดตทั้งสองค่า การสร้างจะล้มเหลว

### <a name="certification-renewal"></a>การต่ออายุใบรับรอง

### <a name="renew-a-certificate-from-trusted-ca"></a>การต่ออายุใบรับรองจาก CA ที่เชื่อถือได้

ติดต่อหน่วยงานออกใบรับรอง (CA) ของคุณสำหรับกระบวนการต่ออายุใบรับรอง สำหรับใบรับรองที่เชื่อถือได้ คุณจะไม่ต้องดำเนินการใดๆ ในฝั่ง MPOS

### <a name="renew-a-self-signed-certificate"></a>ต่ออายุใบรับรองแบบลงนามด้วยตนเอง

อย่าใช้ใบรับรองตัวอย่างที่มีอยู่ใน Retail SDK สำหรับการทำงานจริง เนื่องจากสามารถใช้ได้สำหรับการพัฒนาเท่านั้น ใบรับรอง Contoso ตัวอย่างไม่สามารถต่ออายุได้และใบรับรองตัวอย่างที่รวมอยู่ใน Retail SDK รุ่น 10.0.16 หรือก่อนหน้านั้นหมดอายุลงในวันที่ 31 ธันวาคม 2020 หากใบรับรองนี้หรือใบรับรองแบบลงนามด้วยตนเองมีการใช้เพื่อลงชื่อ Modern POS ที่ปรับแต่ง อาจมีความเป็นไปได้สูงที่ Modern POS จะทำงานไม่ถูกต้องหลังจากวันที่นี้
 
### <a name="impact"></a>ผลกระทบ
 
หากกรณีของคุณเป็นแบบข้างต้น ปัญหาที่คุณจะพบคือตัวติดตั้งจะไม่สามารถทำงานได้หลังจากวันที่ 31 ธันวาคม 2020 Modern POS อาจไม่สามารถใช้งานได้ ทั้งนี้ขึ้นอยู่กับนโยบายด้าน IT ที่บริษัทใช้ เป็นสิ่งสำคัญที่คุณต้องทดสอบเรื่องนี้โดยเปลี่ยนวันที่ชั่วคราวเป็นวันที่ในอนาคตเพื่อตรวจสอบผลกระทบต่อองค์กรของคุณ
 
### <a name="steps-to-determine-the-issue"></a>ขั้นตอนในการระบุปัญหา
 
1.  ใช้การตั้งค่า Windows เพื่อเปลี่ยนนาฬิกาของคอมพิวเตอร์เป็นวันที่และเวลาในปี 2021
2.  ตรวจสอบว่าสามารถเปิด Modern POS ลงชื่อเข้าใช้ได้ และสามารถทำธุรกรรมได้เสร็จสมบูรณ์
3.  ตรวจสอบว่าตัวติดตั้งระบบบริการตนเองของ Modern POS สามารถทำงานได้ และถ้าใช่ แสดงว่าการติดตั้งเสร็จสมบูรณ์
4.  เปลี่ยนการตั้งค่านาฬิกาของ Windows เป็นวันที่และเวลาที่ถูกต้อง
 
ถ้าคุณสามารถดําเนินการขั้นตอนเหล่านี้ทั้งหมดได้โดยไม่มีปัญหา แสดงว่าคุณจะสามารถใช้งานใบรับรองปัจจุบันหลังวันที่ 31 ธันวาคม 2020 ได้  
 
### <a name="steps-going-forward"></a>ขั้นตอนต่อไป 

ขอแนะนำอย่างยิ่งให้คุณต่ออายุใบรับรองที่ใช้ก่อนหน้านี้ เราขอแนะนำให้คุณขอรับใบรับรองใหม่ โดยคุณต้องดำเนินการอย่างหนึ่งอย่างใดต่อไปนี้:
 
- **ที่ต้องการ** - ขอรับใบรับรองการเซ็นโค้ดจากผู้ให้บริการออกใบรับรองที่เชื่อถือได้

- **ไม่ใช่ที่ต้องการ** - สร้างใบรับรองการเซ็นโค้ดแบบลงนามด้วยตนเองที่จะใช้ โดยทั่วไป จะใช้เพื่อวัตถุประสงค์การพัฒนาภายในโดเมนและไม่แนะนะนำให้ใช้สำหรับการทำงานจริง 

- **สามารถใช้งานเป็นวิธีแก้ไขปัญหาชั่วคราว** - ใช้ใบรับรองการเซ็นโค้ด Contoso ที่ต่ออายุ โดยทั่วไปใช้เพื่อวัตถุประสงค์ในการทดสอบ ดังนั้น จึงไม่แนะนำให้ปรับใช้ในการทำงานจริง
 
จากนั้น ให้สร้างแพคเกจ Modern POS แบบปรับแต่งใหม่ ซึ่งลงชื่อโดยใช้ใบรับรองนี้ที่ได้รับมาจากหนึ่งในการดำเนินการข้างต้น ทำตามหนึ่งในขั้นตอนต่อไปนี้ ขึ้นอยู่กับใบรับรอง
 
- หากใช้ใบรับรองที่เชื่อถือได้ใหม่ (ใบรับรองแบบลงนามด้วยตนเองใหม่) คุณจะต้องติดตั้งใบรับรองใหม่บนอุปกรณ์ทุกเครื่อง หลังจากนั้น คุณต้องใช้แพคเกจ Modern POS (ตัวติดตั้ง) ที่สร้างขึ้นใหม่ ถอนการติดตั้งแอปพลิเคชันที่มีอยู่ และติดตั้งแพคเกจ Modern POS ใหม่อีกครั้ง คุณจะต้องมีการเปิดใช้งานอุปกรณ์ของ Modern POS บนอุปกรณ์ทุกเครื่อง

- หากใช้ใบรับรอง Contoso ที่ต่ออายุ คุณจะต้องติดตั้งใบรับรองใหม่บนอุปกรณ์ทุกเครื่องและติดตั้งแพคเกจ Modern POS (ตัวติดตั้ง) คุณอาจไม่ต้องถอนการติดตั้ง แต่คุณต้องติดตั้งใหม่บนอุปกรณ์ โปรดทราบว่าไม่จำเป็นต้องมีการเปิดใช้งานอุปกรณ์ของ Modern POS ตัวเลือกนี้เป็นวิธีแก้ไขปัญหาชั่วคราว ใช้ตัวเลือกนี้เพื่อหลีกเลี่ยงการเปิดใช้งานอีกครั้งและแก้ปัญหาก่อนที่จะขอรับใบรับรองที่เชื่อถือได้ใหม่


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
