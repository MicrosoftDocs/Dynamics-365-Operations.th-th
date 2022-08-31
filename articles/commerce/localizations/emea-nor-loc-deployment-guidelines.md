---
title: แนวทางการปรับใช้เครื่องบันทึกเงินสดสำหรับนอร์เวย์ (ดั้งเดิม)
description: บทความนี้เป็นแนวทางการปรับใช้ที่แสดงวิธีการเปิดใช้งานการแปลเป็นภาษาท้องถิ่น Microsoft Dynamics 365 Commerce สำหรับนอร์เวย์
author: EvgenyPopovMBS
ms.date: 08/23/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2018-2-28
ms.openlocfilehash: fb597add48ac3508a88142e63d80f405b6b5f8b4
ms.sourcegitcommit: 1dbff0b5fa1f4722a1720fac35cce94606fa4320
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/24/2022
ms.locfileid: "9346057"
---
# <a name="deployment-guidelines-for-cash-registers-for-norway-legacy"></a>แนวทางการปรับใช้เครื่องบันทึกเงินสดสำหรับนอร์เวย์ (ดั้งเดิม)

[!include [banner](../includes/banner.md)]

> [!WARNING]
> ตัวอย่างฟังก์ชันการรวมทางการเงินนี้ไม่ได้ใช้ประโยชน์จาก [กรอบงานการรวมทางการเงิน](./fiscal-integration-for-retail-channel.md) และจะไม่สนับสนุนในการอัปเดตในอนาคต คุณควรใช้ [ฟังก์ชันที่ขึ้นอยู่กับกรอบการรวมทางการเงิน](./emea-nor-fi-deployment.md) แทน

บทความนี้เป็นแนวทางการปรับใช้ที่แสดงวิธีการเปิดใช้งานการแปลเป็นภาษาท้องถิ่น Microsoft Dynamics 365 Commerce สำหรับนอร์เวย์ การแปลเป็นภาษาท้องถิ่นประกอบด้วยส่วนขยายของส่วนประกอบของ Commerce หลายส่วน ตัวอย่างเช่น ส่วนขยายช่วยให้คุณสามารถพิมพ์ฟิลด์แบบกำหนดเองบนใบเสร็จ ลงทะเบียนเหตุการณ์การตรวจสอบเพิ่มเติม ธุรกรรมการขาย และธุรกรรมการเงินในการขายหน้าร้าน (POS) ลงชื่อธุรกรรมการขายทางดิจิทัล และพิมพ์รายงาน X และ Z ในรูปแบบท้องถิ่น หากต้องการทราบข้อมูลเพิ่มเติมเกี่ยวกับการแปลเป็นภาษาท้องถิ่นของนอร์เวย์ โปรดดูที่ [ฟังก์ชันเครื่องบันทึกเงินสดสำหรับนอร์เวย์](./emea-nor-cash-registers.md)

ตัวอย่างนี้เป็นส่วนหนึ่งของชุดการพัฒนาซอฟต์แวร์ (SDK) ของการขายปลีก สำหรับข้อมูลเพิ่มเติมเกี่ยวกับ SDK ดูที่ [สถาปัตยกรรมของชุดการพัฒนาซอฟต์แวร์ (SDK) ของการขายปลีก](../dev-itpro/retail-sdk/retail-sdk-overview.md)

ตัวอย่างนี้ประกอบด้วยส่วนขยายของ Commerce Runtime (CRT) เซิร์ฟเวอร์ระบบการขายปลีก และ POS เมื่อต้องการรันตัวอย่างนี้ คุณต้องแก้ไขและสร้าง CRT เซิร์ฟเวอร์ระบบการขายปลีก และโครงการ POS เราขอแนะนำให้คุณใช้ Retail SDK ที่ไม่ได้แก้ไขเพื่อเปลี่ยนแปลงที่อธิบายไว้ในบทความนี้ เราขอแนะนำให้ใช้ระบบควบคุมต้นทาง เช่น Microsoft Visual Studio Online (VSO) โดยที่ยังไม่มีการเปลี่ยนแปลงไฟล์ใดๆ

> [!NOTE]
> ใน Commerce 10.0.8 และสูงกว่า เซิร์ฟเวอร์ระบบการขายปลีกเรียกว่า Commerce Scale Unit เนื่องจากบทความนี้ใช้กับแอปหลายรุ่นก่อนหน้านี้ *เซิร์ฟเวอร์ระบบการขายปลีก* จึงมีการใช้ทั่วทั้งบทความ
>
> บางขั้นตอนในขั้นตอนต่างๆ ในบทความนี้แตกต่างกัน ขึ้นอยู่กับรุ่นของ Commerce ที่คุณใช้อยู่ สำหรับข้อมูลเพิ่มเติม ดูที่ [มีอะไรใหม่หรือมีการเปลี่ยนแปลงอะไรใน Dynamics 365 Retail](../get-started/whats-new.md)

### <a name="using-certificate-profiles-in-commerce-channels"></a>การใช้โปรไฟล์ใบรับรองในช่องทาง Commerce

ใน Commerce รุ่น 10.0.15 และใหม่กว่า คุณสามารถใช้คุณลักษณะ [โปรไฟล์ใบรับรองที่กําหนดโดยผู้ใช้สำหรับร้านค้าปลีก](./certificate-profiles-for-retail-stores.md) ที่รองรับการย้ายโหนดเมื่อเกิดข้อผิดพลาดเกิดขึ้นเป็นออผไลน์เมื่อ Key Vault หรือศูนย์ควบคุม Commerce ไม่พร้อมใช้งาน คุณลักษณะขยายคุณลักษณะ [จัดการข้อมูลความลับของช่องทางการขายปลีก](../dev-itpro/manage-secrets.md)

เมื่อต้องการใช้ฟังก์ชันการใช้งานนี้ในส่วนขยาย CRT ทำตามขั้นตอนเหล่านี้

1. สร้างโครงการส่วนขยาย CRT ใหม่ (ชนิดโครงการของไลบรารีคลาส C#) ใช้แม่แบบตัวอย่างจากชุดการพัฒนาซอฟต์แวร์ (SDK) ของการขายปลีก (RetailSDK\SampleExtensions\CommerceRuntime)

2. เพิ่มตัวจัดการที่ออกแบบเองของ CertificateSignatureServiceRequest ในโครงการ SequentialSignatureRegister

3. เมื่อต้องการอ่านการเรียกข้อมูลลับ `GetUserDefinedSecretCertificateServiceRequest` โดยใช้คอนสตรักเตอร์ที่มีพารามิเตอร์ profileId ซึ่งจะเริ่มต้นฟังก์ชันที่ใช้งานกับการตั้งค่าจากโปรไฟล์ใบรับรอง โดยขึ้นอยู่กับการตั้งค่า ใบรับรองจะถูกดึงข้อมูลจาก Azure Key Vault หรือการจัดเก็บในเครื่องคอมพิวเตอร์

    ```csharp
    GetUserDefinedSecretCertificateServiceRequest getUserDefinedSecretCertificateServiceRequest = new GetUserDefinedSecretCertificateServiceRequest(profileId: "ProfileId", secretName: null, thumbprint: null, expirationInterval: null);
    GetUserDefinedSecretCertificateServiceResponse getUserDefinedSecretCertificateServiceResponse = request.RequestContext.Execute<GetUserDefinedSecretCertificateServiceResponse>(getUserDefinedSecretCertificateServiceRequest);

    X509Certificate2 Certificate = getUserDefinedSecretCertificateServiceResponse.Certificate;
    ```

4. เมื่อดึงข้อมูลใบรับรอง ให้ดําเนินการลงชื่อข้อมูลต่อ

5. สร้างโครงการส่วนขยาย CRT

6. คัดลอกไลบรารีคลาสผลลัพธ์และวางลงใน ...\RetailServer\webroot\bin\Ext เพื่อทดสอบด้วยตนเอง

7. ในไฟล์ CommerceRuntime.Ext.config ให้อัปเดตส่วนขององค์ประกอบส่วนขยายด้วยข้อมูลไลบรารีแบบกำหนดเอง

## <a name="development-environment"></a>สภาพแวดล้อมการพัฒนา

ปฏิบัติตามขั้นตอนต่อไปนี้เพื่อตั้งค่าสภาพแวดล้อมการพัฒนาเพื่อให้คุณสามารถทดสอบและขยายตัวอย่างได้

### <a name="the-crt-extension-components"></a>ส่วนประกอบส่วนขยาย CRT

ส่วนประกอบ CRT ส่วนขยายจะรวมอยู่ในตัวอย่าง CRT เมื่อต้องการปฏิบัติตามขั้นตอนต่อไปนี้ให้เสร็จสมบูรณ์ ให้เปิดโซลูชัน CRT **CommerceRuntimeSamples.sln** ภายใต้ **RetailSdk\\SampleExtensions\\CommerceRuntime**

#### <a name="receiptsnorway-component"></a>ส่วนประกอบ ReceiptsNorway

1. ค้นหาโครงการ **Runtime.Extensions.ReceiptsNorway** และสร้าง
2. ในโฟลเดอร์ **Extensions.ReceiptsNorway\\bin\\Debug** ให้ค้นหาไฟล์แอสเซมบลี **Contoso.Commerce.Runtime.ReceiptsNorway.dll**
3. คัดลอกไฟล์แอสเซมบลีไปยังโฟลเดอร์ส่วนขยาย CRT:

    - **เซิร์ฟเวอร์ระบบการขายปลีก:** คัดลอกแอสเซมบลีไปยังโฟลเดอร์ **\\bin\\ext** ภายใต้ที่ตั้งไซต์เซิร์ฟเวอร์ระบบการขายปลีกของ Microsoft Internet Information Services (IIS)
    - **CRT ท้องถิ่นบน POS สมัยใหม่:** คัดลอกแอสเซมบลีไปยังโฟลเดอร์ **\\ext** ภายใต้ที่ตั้งของ Client Broker ของ CRT ท้องถิ่น

4. ค้นหาไฟล์การกำหนดค่าส่วนขยายสำหรับ CRT:

    - **เซิร์ฟเวอร์ระบบการขายปลีก:** ไฟล์มีชื่อว่า **commerceruntime.ext.config** และอยู่ในโฟลเดอร์ **bin\\ext** ภายใต้ที่ตั้งไซต์เซิร์ฟเวอร์ระบบการขายปลีก IIS
    - **CRT เฉพาะที่บน Modern POS:** ไฟล์มีชื่อว่า **CommerceRuntime.MPOSOffline.Ext.config** และอยู่ภายใต้ที่ตั้ง Client Broker ของ CRT เฉพาะที่

5. ลงทะเบียนการเปลี่ยนแปลง CRT ในไฟล์การกำหนดค่าส่วนขยาย

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
    ```

    > [!WARNING]
    > ห้าม **ไม่ให้** แก้ไขไฟล์ commerceruntime.config และ CommerceRuntime.MPOSOffline.config ไฟล์เหล่านี้ไม่ได้มีไว้เพื่อการกำหนดเองใดๆ

#### <a name="salespaymenttransext-component"></a>ส่วนประกอบ SalesPaymentTransExt

1. ค้นหาโครงการ **Runtime.Extensions.SalesPaymentTransExt** และสร้าง
2. ในโฟลเดอร์ **Extensions.SalesPaymentTransExt\\bin\\Debug** ให้ค้นหาไฟล์แอสเซมบลี **Contoso.Commerce.Runtime.SalesPaymentTransExt.dll**
3. คัดลอกไฟล์แอสเซมบลีไปยังโฟลเดอร์ส่วนขยาย CRT:

    - **เซิร์ฟเวอร์ระบบการขายปลีก:** คัดลอกแอสเซมบลีไปยังโฟลเดอร์ **\\bin\\ext** ภายใต้ที่ตั้งไซต์เซิร์ฟเวอร์ระบบการขายปลีกของ IIS
    - **CRT ท้องถิ่นบน POS สมัยใหม่:** คัดลอกแอสเซมบลีไปยังโฟลเดอร์ **\\ext** ภายใต้ที่ตั้งของ Client Broker ของ CRT ท้องถิ่น

4. ค้นหาไฟล์การกำหนดค่าส่วนขยายสำหรับ CRT:

    - **เซิร์ฟเวอร์ระบบการขายปลีก:** ไฟล์มีชื่อว่า **commerceruntime.ext.config** และอยู่ในโฟลเดอร์ **bin\\ext** ภายใต้ที่ตั้งไซต์เซิร์ฟเวอร์ระบบการขายปลีก IIS
    - **CRT เฉพาะที่บน Modern POS:** ไฟล์มีชื่อว่า **CommerceRuntime.MPOSOffline.Ext.config** และอยู่ภายใต้ที่ตั้ง Client Broker ของ CRT เฉพาะที่

5. ลงทะเบียนการเปลี่ยนแปลง CRT ในไฟล์การกำหนดค่าส่วนขยาย

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
    ```

    > [!WARNING]
    > ห้าม **ไม่ให้** แก้ไขไฟล์ commerceruntime.config และ CommerceRuntime.MPOSOffline.config ไฟล์เหล่านี้ไม่ได้มีไว้เพื่อการกำหนดเองใดๆ

#### <a name="xzreportsnorway-component"></a>ส่วนประกอบ XZReportsNorway

1. ค้นหาโครงการ **Runtime.Extensions.XZReportsNorway** และสร้าง
2. ในโฟลเดอร์ **Extensions.XZReportsNorway\\bin\\Debug** ให้ค้นหาไฟล์แอสเซมบลี **Contoso.Commerce.Runtime.XZReportsNorway.dll**
3. คัดลอกไฟล์แอสเซมบลีไปยังโฟลเดอร์ส่วนขยาย CRT:

    - **เซิร์ฟเวอร์ระบบการขายปลีก:** คัดลอกแอสเซมบลีไปยังโฟลเดอร์ **\\bin\\ext** ภายใต้ที่ตั้งไซต์เซิร์ฟเวอร์ระบบการขายปลีกของ IIS
    - **CRT ท้องถิ่นบน POS สมัยใหม่:** คัดลอกแอสเซมบลีไปยังโฟลเดอร์ **\\ext** ภายใต้ที่ตั้งของ Client Broker ของ CRT ท้องถิ่น

4. ค้นหาไฟล์การกำหนดค่าส่วนขยายสำหรับ CRT:

    - **เซิร์ฟเวอร์ระบบการขายปลีก:** ไฟล์มีชื่อว่า **commerceruntime.ext.config** และอยู่ในโฟลเดอร์ **bin\\ext** ภายใต้ที่ตั้งไซต์เซิร์ฟเวอร์ระบบการขายปลีก IIS
    - **CRT เฉพาะที่บน Modern POS:** ไฟล์มีชื่อว่า **CommerceRuntime.MPOSOffline.Ext.config** และอยู่ภายใต้ที่ตั้ง Client Broker ของ CRT เฉพาะที่

5. ลงทะเบียนการเปลี่ยนแปลง CRT ในไฟล์การกำหนดค่าส่วนขยาย

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
    ```

    > [!WARNING]
    > ห้าม **ไม่ให้** แก้ไขไฟล์ commerceruntime.config และ CommerceRuntime.MPOSOffline.config ไฟล์เหล่านี้ไม่ได้มีไว้เพื่อการกำหนดเองใดๆ

# <a name="application-update-4"></a>[Application update 4](#tab/app-update-4)

#### <a name="registerauditevent-sample-component"></a>ส่วนประกอบตัวอย่าง RegisterAuditEvent

1. ค้นหาโครงการ **Runtime.Extensions.RegisterAuditEventSample** และสร้าง
2. ในโฟลเดอร์ **Extensions.RegisterAuditEventSample\\bin\\Debug** ให้ค้นหาไฟล์แอสเซมบลี **Contoso.Commerce.Runtime.RegisterAuditEventSample.dll**
3. คัดลอกไฟล์แอสเซมบลีไปยังโฟลเดอร์ส่วนขยาย CRT:

    - **เซิร์ฟเวอร์ระบบการขายปลีก:** คัดลอกแอสเซมบลีไปยังโฟลเดอร์ **\\bin\\ext** ภายใต้ที่ตั้งไซต์เซิร์ฟเวอร์ระบบการขายปลีกของ IIS
    - **CRT ท้องถิ่นบน POS สมัยใหม่:** คัดลอกแอสเซมบลีไปยังโฟลเดอร์ **\\ext** ภายใต้ที่ตั้งของ Client Broker ของ CRT ท้องถิ่น

4. ค้นหาไฟล์การกำหนดค่าส่วนขยายสำหรับ CRT:

    - **เซิร์ฟเวอร์ระบบการขายปลีก:** ไฟล์มีชื่อว่า **commerceruntime.ext.config** และอยู่ในโฟลเดอร์ **bin\\ext** ภายใต้ที่ตั้งไซต์เซิร์ฟเวอร์ระบบการขายปลีก IIS
    - **CRT เฉพาะที่บน Modern POS:** ไฟล์มีชื่อว่า **CommerceRuntime.MPOSOffline.Ext.config** และอยู่ภายใต้ที่ตั้ง Client Broker ของ CRT เฉพาะที่

5. ลงทะเบียนการเปลี่ยนแปลง CRT ในไฟล์การกำหนดค่าส่วนขยาย

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
    ```

    > [!WARNING]
    > ห้าม **ไม่ให้** แก้ไขไฟล์ commerceruntime.config และ CommerceRuntime.MPOSOffline.config ไฟล์เหล่านี้ไม่ได้มีไว้เพื่อการกำหนดเองใดๆ

#### <a name="salestransactionsignature-sample-component"></a>ส่วนประกอบตัวอย่าง SalesTransactionSignature

1. ค้นหาโครงการ **Runtime.Extensions.SalesTransactionSignatureSample**
2. แก้ไขไฟล์ **App.config** โดยระบุรหัสประจำตัว ที่ตั้งร้านค้า และชื่อร้านค้าของใบรับรองที่ควรใช้ในการลงชื่อธุรกรรมการขาย
3. สร้างโครงการ
4. ในโฟลเดอร์ **Extensions.SalesTransactionSignatureSample\\bin\\Debug** ค้นหาไฟล์ต่อไปนี้:

    - ไฟล์แอสเซมบลี **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll**
    - ไฟล์การกำหนดค่า **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config**

5. คัดลอกไฟล์ไปยังโฟลเดอร์ส่วนขยาย CRT:

    - **เซิร์ฟเวอร์ระบบการขายปลีก:** คัดลอกแอสเซมบลีไปยังโฟลเดอร์ **\\bin\\ext** ภายใต้ที่ตั้งไซต์เซิร์ฟเวอร์ระบบการขายปลีกของ IIS
    - **CRT ท้องถิ่นบน POS สมัยใหม่:** คัดลอกแอสเซมบลีไปยังโฟลเดอร์ **\\ext** ภายใต้ที่ตั้งของ Client Broker ของ CRT ท้องถิ่น

6. ค้นหาไฟล์การกำหนดค่าส่วนขยายสำหรับ CRT:

    - **เซิร์ฟเวอร์ระบบการขายปลีก:** ไฟล์มีชื่อว่า **commerceruntime.ext.config** และอยู่ในโฟลเดอร์ **bin\\ext** ภายใต้ที่ตั้งไซต์เซิร์ฟเวอร์ระบบการขายปลีก IIS
    - **CRT เฉพาะที่บน Modern POS:** ไฟล์มีชื่อว่า **CommerceRuntime.MPOSOffline.Ext.config** และอยู่ภายใต้ที่ตั้ง Client Broker ของ CRT เฉพาะที่

7. ลงทะเบียนการเปลี่ยนแปลง CRT ในไฟล์การกำหนดค่าส่วนขยาย

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
    ```

    > [!WARNING]
    > ห้าม **ไม่ให้** แก้ไขไฟล์ commerceruntime.config และ CommerceRuntime.MPOSOffline.config ไฟล์เหล่านี้ไม่ได้มีไว้เพื่อการกำหนดเองใดๆ

# <a name="application-update-5-and-later"></a>[Application update 5 และรุ่นใหม่กว่า](#tab/app-update-5-and-later)

#### <a name="registerauditevent-sample-component"></a>ส่วนประกอบตัวอย่าง RegisterAuditEvent

1. ค้นหาโครงการ **Runtime.Extensions.RegisterAuditEventSample** และสร้าง
2. ในโฟลเดอร์ **Extensions.RegisterAuditEventSample\\bin\\Debug** ให้ค้นหาไฟล์แอสเซมบลี **Contoso.Commerce.Runtime.RegisterAuditEventSample.dll**
3. คัดลอกไฟล์แอสเซมบลีไปยังโฟลเดอร์ส่วนขยาย CRT:

    - **เซิร์ฟเวอร์ระบบการขายปลีก:** คัดลอกแอสเซมบลีไปยังโฟลเดอร์ **\\bin\\ext** ภายใต้ที่ตั้งไซต์เซิร์ฟเวอร์ระบบการขายปลีกของ IIS
    - **CRT ท้องถิ่นบน POS สมัยใหม่:** คัดลอกแอสเซมบลีไปยังโฟลเดอร์ **\\ext** ภายใต้ที่ตั้งของ Client Broker ของ CRT ท้องถิ่น

4. ค้นหาไฟล์การกำหนดค่าส่วนขยายสำหรับ CRT:

    - **เซิร์ฟเวอร์ระบบการขายปลีก:** ไฟล์มีชื่อว่า **commerceruntime.ext.config** และอยู่ในโฟลเดอร์ **bin\\ext** ภายใต้ที่ตั้งไซต์เซิร์ฟเวอร์ระบบการขายปลีก IIS
    - **CRT เฉพาะที่บน Modern POS:** ไฟล์มีชื่อว่า **CommerceRuntime.MPOSOffline.Ext.config** และอยู่ภายใต้ที่ตั้ง Client Broker ของ CRT เฉพาะที่

5. ลงทะเบียนการเปลี่ยนแปลง CRT ในไฟล์การกำหนดค่าส่วนขยาย

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
    ```

    > [!WARNING]
    > ห้าม **ไม่ให้** แก้ไขไฟล์ commerceruntime.config และ CommerceRuntime.MPOSOffline.config ไฟล์เหล่านี้ไม่ได้มีไว้เพื่อการกำหนดเองใดๆ

#### <a name="salestransactionsignature-sample-component"></a>ส่วนประกอบตัวอย่าง SalesTransactionSignature

1. ค้นหาโครงการ **Runtime.Extensions.SalesTransactionSignatureSample**
2. แก้ไขไฟล์ **App.config** โดยระบุรหัสประจำตัว ที่ตั้งร้านค้า และชื่อร้านค้าของใบรับรองที่ควรใช้ในการลงชื่อธุรกรรมการขาย
3. สร้างโครงการ
4. ในโฟลเดอร์ **Extensions.SalesTransactionSignatureSample\\bin\\Debug** ค้นหาไฟล์ต่อไปนี้:

    - ไฟล์แอสเซมบลี **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll**
    - ไฟล์การกำหนดค่า **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config**

5. คัดลอกไฟล์ไปยังโฟลเดอร์ส่วนขยาย CRT:

    - **เซิร์ฟเวอร์ระบบการขายปลีก:** คัดลอกแอสเซมบลีไปยังโฟลเดอร์ **\\bin\\ext** ภายใต้ที่ตั้งไซต์เซิร์ฟเวอร์ระบบการขายปลีกของ IIS
    - **CRT ท้องถิ่นบน POS สมัยใหม่:** คัดลอกแอสเซมบลีไปยังโฟลเดอร์ **\\ext** ภายใต้ที่ตั้งของ Client Broker ของ CRT ท้องถิ่น

6. ค้นหาไฟล์การกำหนดค่าส่วนขยายสำหรับ CRT:

    - **เซิร์ฟเวอร์ระบบการขายปลีก:** ไฟล์มีชื่อว่า **commerceruntime.ext.config** และอยู่ในโฟลเดอร์ **bin\\ext** ภายใต้ที่ตั้งไซต์เซิร์ฟเวอร์ระบบการขายปลีก IIS
    - **CRT เฉพาะที่บน Modern POS:** ไฟล์มีชื่อว่า **CommerceRuntime.MPOSOffline.Ext.config** และอยู่ภายใต้ที่ตั้ง Client Broker ของ CRT เฉพาะที่

7. ลงทะเบียนการเปลี่ยนแปลง CRT ในไฟล์การกำหนดค่าส่วนขยาย

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
    ```

    > [!WARNING]
    > ห้าม **ไม่ให้** แก้ไขไฟล์ commerceruntime.config และ CommerceRuntime.MPOSOffline.config ไฟล์เหล่านี้ไม่ได้มีไว้เพื่อการกำหนดเองใดๆ

#### <a name="salestransactionsignaturesamplemessages-component"></a>ส่วนประกอบ SalesTransactionSignatureSample.Messages

1. ค้นหาโครงการ **Runtime.Extensions.SalesTransactionSignatureSample.Messages**
2. ในโฟลเดอร์ **Extensions.SalesTransactionSignatureSample.Messages\\bin\\Debug** ให้ค้นหาไฟล์แอสเซมบลี **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages.dll**
3. คัดลอกไฟล์แอสเซมบลีไปยังโฟลเดอร์ส่วนขยาย CRT:

    - **เซิร์ฟเวอร์ระบบการขายปลีก:** คัดลอกแอสเซมบลีไปยังโฟลเดอร์ **\\bin\\ext** ภายใต้ที่ตั้งไซต์เซิร์ฟเวอร์ระบบการขายปลีกของ IIS
    - **CRT ท้องถิ่นบน POS สมัยใหม่:** คัดลอกแอสเซมบลีไปยังโฟลเดอร์ **\\ext** ภายใต้ที่ตั้งของ Client Broker ของ CRT ท้องถิ่น

4. ค้นหาไฟล์การกำหนดค่าส่วนขยายสำหรับ CRT:

    - **เซิร์ฟเวอร์ระบบการขายปลีก:** ไฟล์มีชื่อว่า **commerceruntime.ext.config** และอยู่ในโฟลเดอร์ **bin\\ext** ภายใต้ที่ตั้งไซต์เซิร์ฟเวอร์ระบบการขายปลีก IIS
    - **CRT เฉพาะที่บน Modern POS:** ไฟล์มีชื่อว่า **CommerceRuntime.MPOSOffline.Ext.config** และอยู่ภายใต้ที่ตั้ง Client Broker ของ CRT เฉพาะที่

5. ลงทะเบียนการเปลี่ยนแปลง CRT ในไฟล์การกำหนดค่าส่วนขยาย

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages" />
    ```

    > [!WARNING]
    > ห้าม **ไม่ให้** แก้ไขไฟล์ commerceruntime.config และ CommerceRuntime.MPOSOffline.config ไฟล์เหล่านี้ไม่ได้มีไว้เพื่อการกำหนดเองใดๆ

# <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

#### <a name="registerauditevent-sample-component"></a>ส่วนประกอบตัวอย่าง RegisterAuditEvent

1. ค้นหาโครงการ **Runtime.Extensions.RegisterAuditEventSample** และสร้าง
2. ในโฟลเดอร์ **Extensions.RegisterAuditEventSample\\bin\\Debug** ให้ค้นหาไฟล์แอสเซมบลี **Contoso.Commerce.Runtime.RegisterAuditEventSample.dll**
3. คัดลอกไฟล์แอสเซมบลีไปยังโฟลเดอร์ส่วนขยาย CRT:

    - **เซิร์ฟเวอร์ระบบการขายปลีก:** คัดลอกแอสเซมบลีไปยังโฟลเดอร์ **\\bin\\ext** ภายใต้ที่ตั้งไซต์เซิร์ฟเวอร์ระบบการขายปลีกของ IIS
    - **CRT ท้องถิ่นบน POS สมัยใหม่:** คัดลอกแอสเซมบลีไปยังโฟลเดอร์ **\\ext** ภายใต้ที่ตั้งของ Client Broker ของ CRT ท้องถิ่น

4. ค้นหาไฟล์การกำหนดค่าส่วนขยายสำหรับ CRT:

    - **เซิร์ฟเวอร์ระบบการขายปลีก:** ไฟล์มีชื่อว่า **commerceruntime.ext.config** และอยู่ในโฟลเดอร์ **bin\\ext** ภายใต้ที่ตั้งไซต์เซิร์ฟเวอร์ระบบการขายปลีก IIS
    - **CRT เฉพาะที่บน Modern POS:** ไฟล์มีชื่อว่า **CommerceRuntime.MPOSOffline.Ext.config** และอยู่ภายใต้ที่ตั้ง Client Broker ของ CRT เฉพาะที่

5. ลงทะเบียนการเปลี่ยนแปลง CRT ในไฟล์การกำหนดค่าส่วนขยาย

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
    ```

    > [!WARNING]
    > ห้าม **ไม่ให้** แก้ไขไฟล์ commerceruntime.config และ CommerceRuntime.MPOSOffline.config ไฟล์เหล่านี้ไม่ได้มีไว้เพื่อการกำหนดเองใดๆ

#### <a name="salestransactionsignature-sample-component"></a>ส่วนประกอบตัวอย่าง SalesTransactionSignature

1. ค้นหาโครงการ **Runtime.Extensions.SalesTransactionSignatureSample**
2. แก้ไขไฟล์ **App.config** โดยระบุรหัสประจำตัว ที่ตั้งร้านค้า และชื่อร้านค้าของใบรับรองที่ควรใช้ในการลงชื่อธุรกรรมการขาย
3. สร้างโครงการ
4. ในโฟลเดอร์ **Extensions.SalesTransactionSignatureSample\\bin\\Debug** ค้นหาไฟล์ต่อไปนี้:

    - ไฟล์แอสเซมบลี **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll**
    - ไฟล์การกำหนดค่า **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config**

5. คัดลอกไฟล์ไปยังโฟลเดอร์ส่วนขยาย CRT:

    - **เซิร์ฟเวอร์ระบบการขายปลีก:** คัดลอกแอสเซมบลีไปยังโฟลเดอร์ **\\bin\\ext** ภายใต้ที่ตั้งไซต์เซิร์ฟเวอร์ระบบการขายปลีกของ IIS
    - **CRT ท้องถิ่นบน POS สมัยใหม่:** คัดลอกแอสเซมบลีไปยังโฟลเดอร์ **\\ext** ภายใต้ที่ตั้งของ Client Broker ของ CRT ท้องถิ่น

6. ค้นหาไฟล์การกำหนดค่าส่วนขยายสำหรับ CRT:

    - **เซิร์ฟเวอร์ระบบการขายปลีก:** ไฟล์มีชื่อว่า **commerceruntime.ext.config** และอยู่ในโฟลเดอร์ **bin\\ext** ภายใต้ที่ตั้งไซต์เซิร์ฟเวอร์ระบบการขายปลีก IIS
    - **CRT เฉพาะที่บน Modern POS:** ไฟล์มีชื่อว่า **CommerceRuntime.MPOSOffline.Ext.config** และอยู่ภายใต้ที่ตั้ง Client Broker ของ CRT เฉพาะที่

7. ลงทะเบียนการเปลี่ยนแปลง CRT ในไฟล์การกำหนดค่าส่วนขยาย

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
    ```

    > [!WARNING]
    > ห้าม **ไม่ให้** แก้ไขไฟล์ commerceruntime.config และ CommerceRuntime.MPOSOffline.config ไฟล์เหล่านี้ไม่ได้มีไว้เพื่อการกำหนดเองใดๆ

#### <a name="sequentialsignatureregistercontracts-component"></a>ส่วนประกอบ SequentialSignatureRegister.Contracts

1. ค้นหาโครงการ **Runtime.Extensions.SequentialSignatureRegister.Contracts**
2. ในโฟลเดอร์ **Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug** ให้ค้นหาไฟล์แอสเซมบลี **Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll**
3. คัดลอกไฟล์แอสเซมบลีไปยังโฟลเดอร์ส่วนขยาย CRT:

    - **เซิร์ฟเวอร์ระบบการขายปลีก:** คัดลอกแอสเซมบลีไปยังโฟลเดอร์ **\\bin\\ext** ภายใต้ที่ตั้งไซต์เซิร์ฟเวอร์ระบบการขายปลีกของ IIS
    - **CRT ท้องถิ่นบน POS สมัยใหม่:** คัดลอกแอสเซมบลีไปยังโฟลเดอร์ **\\ext** ภายใต้ที่ตั้งของ Client Broker ของ CRT ท้องถิ่น

# <a name="retail-732-and-later"></a>[Retail 7.3.2 และรุ่นที่ใหม่กว่า](#tab/retail-7-3-2)

#### <a name="registerauditevent-sample-component"></a>ส่วนประกอบตัวอย่าง RegisterAuditEvent

1. ค้นหาโครงการ **Runtime.Extensions.RegisterAuditEventSample** และสร้าง
2. ในโฟลเดอร์ **Extensions.RegisterAuditEventSample\\bin\\Debug** ให้ค้นหาไฟล์แอสเซมบลี **Contoso.Commerce.Runtime.RegisterAuditEventSample.dll**
3. คัดลอกไฟล์แอสเซมบลีไปยังโฟลเดอร์ส่วนขยาย CRT:

    - **เซิร์ฟเวอร์ระบบการขายปลีก:** คัดลอกแอสเซมบลีไปยังโฟลเดอร์ **\\bin\\ext** ภายใต้ที่ตั้งไซต์เซิร์ฟเวอร์ระบบการขายปลีกของ IIS
    - **CRT ท้องถิ่นบน POS สมัยใหม่:** คัดลอกแอสเซมบลีไปยังโฟลเดอร์ **\\ext** ภายใต้ที่ตั้งของ Client Broker ของ CRT ท้องถิ่น

4. ค้นหาไฟล์การกำหนดค่าส่วนขยายสำหรับ CRT:

    - **เซิร์ฟเวอร์ระบบการขายปลีก:** ไฟล์มีชื่อว่า **commerceruntime.ext.config** และอยู่ในโฟลเดอร์ **bin\\ext** ภายใต้ที่ตั้งไซต์เซิร์ฟเวอร์ระบบการขายปลีก IIS
    - **CRT เฉพาะที่บน Modern POS:** ไฟล์มีชื่อว่า **CommerceRuntime.MPOSOffline.Ext.config** และอยู่ภายใต้ที่ตั้ง Client Broker ของ CRT เฉพาะที่

5. ลงทะเบียนการเปลี่ยนแปลง CRT ในไฟล์การกำหนดค่าส่วนขยาย

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
    ```

    > [!WARNING]
    > ห้าม **ไม่ให้** แก้ไขไฟล์ commerceruntime.config และ CommerceRuntime.MPOSOffline.config ไฟล์เหล่านี้ไม่ได้มีไว้เพื่อการกำหนดเองใดๆ

#### <a name="sequentialsignatureregister-component"></a>ส่วนประกอบ SequentialSignatureRegister

1. ค้นหาโครงการ **Runtime.Extensions.SequentialSignatureRegister**
2. แก้ไขไฟล์ **App.config** โดยระบุรหัสประจำตัว ที่ตั้งร้านค้า และชื่อร้านค้าของใบรับรองที่ควรใช้ในการลงชื่อธุรกรรมการขาย
3. สร้างโครงการ
4. ในโฟลเดอร์ **Extensions.SequentialSignatureRegister\\bin\\Debug** ค้นหาไฟล์ต่อไปนี้:

    - ไฟล์แอสเซมบลี **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll**
    - ไฟล์การกำหนดค่า **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config**

5. คัดลอกไฟล์ไปยังโฟลเดอร์ส่วนขยาย CRT:

    - **เซิร์ฟเวอร์ระบบการขายปลีก:** คัดลอกแอสเซมบลีไปยังโฟลเดอร์ **\\bin\\ext** ภายใต้ที่ตั้งไซต์เซิร์ฟเวอร์ระบบการขายปลีกของ IIS
    - **CRT ท้องถิ่นบน POS สมัยใหม่:** คัดลอกแอสเซมบลีไปยังโฟลเดอร์ **\\ext** ภายใต้ที่ตั้งของ Client Broker ของ CRT ท้องถิ่น

6. ค้นหาไฟล์การกำหนดค่าส่วนขยายสำหรับ CRT:

    - **เซิร์ฟเวอร์ระบบการขายปลีก:** ไฟล์มีชื่อว่า **commerceruntime.ext.config** และอยู่ในโฟลเดอร์ **bin\\ext** ภายใต้ที่ตั้งไซต์เซิร์ฟเวอร์ระบบการขายปลีก IIS
    - **CRT เฉพาะที่บน Modern POS:** ไฟล์มีชื่อว่า **CommerceRuntime.MPOSOffline.Ext.config** และอยู่ภายใต้ที่ตั้ง Client Broker ของ CRT เฉพาะที่

7. ลงทะเบียนการเปลี่ยนแปลง CRT ในไฟล์การกำหนดค่าส่วนขยาย

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
    ```

    > [!WARNING]
    > ห้าม **ไม่ให้** แก้ไขไฟล์ commerceruntime.config และ CommerceRuntime.MPOSOffline.config ไฟล์เหล่านี้ไม่ได้มีไว้เพื่อการกำหนดเองใดๆ

#### <a name="salestransactionsignaturenorway-component"></a>ส่วนประกอบ SalesTransactionSignatureNorway

1. ค้นหาโครงการ **Runtime.Extensions.SalesTransactionSignatureNorway**
2. ในโฟลเดอร์ **Extensions.SalesTransactionSignatureNorway\\bin\\Debug** ให้ค้นหาไฟล์แอสเซมบลี **Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll**
3. คัดลอกไฟล์แอสเซมบลีไปยังโฟลเดอร์ส่วนขยาย CRT:

    - **เซิร์ฟเวอร์ระบบการขายปลีก:** คัดลอกแอสเซมบลีไปยังโฟลเดอร์ **\\bin\\ext** ภายใต้ที่ตั้งไซต์เซิร์ฟเวอร์ระบบการขายปลีกของ IIS
    - **CRT ท้องถิ่นบน POS สมัยใหม่:** คัดลอกแอสเซมบลีไปยังโฟลเดอร์ **\\ext** ภายใต้ที่ตั้งของ Client Broker ของ CRT ท้องถิ่น

4. ค้นหาไฟล์การกำหนดค่าส่วนขยายสำหรับ CRT:

    - **เซิร์ฟเวอร์ระบบการขายปลีก:** ไฟล์มีชื่อว่า **commerceruntime.ext.config** และอยู่ในโฟลเดอร์ **bin\\ext** ภายใต้ที่ตั้งไซต์เซิร์ฟเวอร์ระบบการขายปลีก IIS
    - **CRT เฉพาะที่บน Modern POS:** ไฟล์มีชื่อว่า **CommerceRuntime.MPOSOffline.Ext.config** และอยู่ภายใต้ที่ตั้ง Client Broker ของ CRT เฉพาะที่

5. ลงทะเบียนการเปลี่ยนแปลง CRT ในไฟล์การกำหนดค่าส่วนขยาย

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
    ```

    > [!WARNING]
    > ห้าม **ไม่ให้** แก้ไขไฟล์ commerceruntime.config และ CommerceRuntime.MPOSOffline.config ไฟล์เหล่านี้ไม่ได้มีไว้เพื่อการกำหนดเองใดๆ

#### <a name="sequentialsignatureregistercontracts-component"></a>ส่วนประกอบ SequentialSignatureRegister.Contracts

1. ค้นหาโครงการ **Runtime.Extensions.SequentialSignatureRegister.Contracts**
2. ในโฟลเดอร์ **Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug** ให้ค้นหาไฟล์แอสเซมบลี **Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll**
3. คัดลอกไฟล์แอสเซมบลีไปยังโฟลเดอร์ส่วนขยาย CRT:

    - **เซิร์ฟเวอร์ระบบการขายปลีก:** คัดลอกแอสเซมบลีไปยังโฟลเดอร์ **\\bin\\ext** ภายใต้ที่ตั้งไซต์เซิร์ฟเวอร์ระบบการขายปลีกของ IIS
    - **CRT ท้องถิ่นบน POS สมัยใหม่:** คัดลอกแอสเซมบลีไปยังโฟลเดอร์ **\\ext** ภายใต้ที่ตั้งของ Client Broker ของ CRT ท้องถิ่น

#### <a name="salespaymenttransextnorway-component"></a>ส่วนประกอบ SalesPaymentTransExtNorway

1. ค้นหาโครงการ **Runtime.Extensions.SalesPaymentTransExtNorway** และสร้าง
2. ในโฟลเดอร์ **Extensions.SalesPaymentTransExtNorway\\bin\\Debug** ให้ค้นหาไฟล์แอสเซมบลี **Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll**
3. คัดลอกไฟล์แอสเซมบลีไปยังโฟลเดอร์ส่วนขยาย CRT:

    - **เซิร์ฟเวอร์ระบบการขายปลีก:** คัดลอกแอสเซมบลีไปยังโฟลเดอร์ **\\bin\\ext** ภายใต้ที่ตั้งไซต์เซิร์ฟเวอร์ระบบการขายปลีกของ IIS
    - **CRT ท้องถิ่นบน POS สมัยใหม่:** คัดลอกแอสเซมบลีไปยังโฟลเดอร์ **\\ext** ภายใต้ที่ตั้งของ Client Broker ของ CRT ท้องถิ่น

4. ค้นหาไฟล์การกำหนดค่าส่วนขยายสำหรับ CRT:

    - **เซิร์ฟเวอร์ระบบการขายปลีก:** ไฟล์มีชื่อว่า **commerceruntime.ext.config** และอยู่ในโฟลเดอร์ **bin\\ext** ภายใต้ที่ตั้งไซต์เซิร์ฟเวอร์ระบบการขายปลีก IIS
    - **CRT เฉพาะที่บน Modern POS:** ไฟล์มีชื่อว่า **CommerceRuntime.MPOSOffline.Ext.config** และอยู่ภายใต้ที่ตั้ง Client Broker ของ CRT เฉพาะที่

5. ลงทะเบียนการเปลี่ยนแปลง CRT ในไฟล์การกำหนดค่าส่วนขยาย

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
    ```

    > [!WARNING]
    > ห้าม **ไม่ให้** แก้ไขไฟล์ commerceruntime.config และ CommerceRuntime.MPOSOffline.config ไฟล์เหล่านี้ไม่ได้มีไว้เพื่อการกำหนดเองใดๆ

# <a name="retail-735-and-later"></a>[Retail 7.3.5 และรุ่นที่ใหม่กว่า](#tab/retail-7-3-5)

#### <a name="registerauditeventnorway-component"></a>ส่วนประกอบ RegisterAuditEventNorway

1. ค้นหาไฟล์การกำหนดค่าส่วนขยายสำหรับ CRT:

    - **เซิร์ฟเวอร์ระบบการขายปลีก:** ไฟล์มีชื่อว่า **commerceruntime.ext.config** และอยู่ในโฟลเดอร์ **bin\\ext** ภายใต้ที่ตั้งไซต์เซิร์ฟเวอร์ระบบการขายปลีก IIS
    - **CRT เฉพาะที่บน Modern POS:** ไฟล์มีชื่อว่า **CommerceRuntime.MPOSOffline.Ext.config** และอยู่ภายใต้ที่ตั้ง Client Broker ของ CRT เฉพาะที่

2. ลงทะเบียนการเปลี่ยนแปลง CRT ในไฟล์การกำหนดค่าส่วนขยาย

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventNorway" />
    ```

    > [!WARNING]
    > ห้าม **ไม่ให้** แก้ไขไฟล์ commerceruntime.config และ CommerceRuntime.MPOSOffline.config ไฟล์เหล่านี้ไม่ได้มีไว้เพื่อการกำหนดเองใดๆ

#### <a name="sequentialsignatureregister-component"></a>ส่วนประกอบ SequentialSignatureRegister

1. ค้นหาโครงการ **Runtime.Extensions.SequentialSignatureRegister**
2. แก้ไขไฟล์ **App.config** โดยระบุรหัสประจำตัว ที่ตั้งร้านค้า และชื่อร้านค้าของใบรับรองที่ควรใช้ในการลงชื่อธุรกรรมการขาย
3. สร้างโครงการ
4. ในโฟลเดอร์ **Extensions.SequentialSignatureRegister\\bin\\Debug** ค้นหาไฟล์ต่อไปนี้:

    - ไฟล์แอสเซมบลี **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll**
    - ไฟล์การกำหนดค่า **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config**

5. คัดลอกไฟล์ไปยังโฟลเดอร์ส่วนขยาย CRT:

    - **เซิร์ฟเวอร์ระบบการขายปลีก:** คัดลอกแอสเซมบลีไปยังโฟลเดอร์ **\\bin\\ext** ภายใต้ที่ตั้งไซต์เซิร์ฟเวอร์ระบบการขายปลีกของ IIS
    - **CRT ท้องถิ่นบน POS สมัยใหม่:** คัดลอกแอสเซมบลีไปยังโฟลเดอร์ **\\ext** ภายใต้ที่ตั้งของ Client Broker ของ CRT ท้องถิ่น

6. ค้นหาไฟล์การกำหนดค่าส่วนขยายสำหรับ CRT:

    - **เซิร์ฟเวอร์ระบบการขายปลีก:** ไฟล์มีชื่อว่า **commerceruntime.ext.config** และอยู่ในโฟลเดอร์ **bin\\ext** ภายใต้ที่ตั้งไซต์เซิร์ฟเวอร์ระบบการขายปลีก IIS
    - **CRT เฉพาะที่บน Modern POS:** ไฟล์มีชื่อว่า **CommerceRuntime.MPOSOffline.Ext.config** และอยู่ภายใต้ที่ตั้ง Client Broker ของ CRT เฉพาะที่

7. ลงทะเบียนการเปลี่ยนแปลง CRT ในไฟล์การกำหนดค่าส่วนขยาย

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
    ```

    > [!WARNING]
    > ห้าม **ไม่ให้** แก้ไขไฟล์ commerceruntime.config และ CommerceRuntime.MPOSOffline.config ไฟล์เหล่านี้ไม่ได้มีไว้เพื่อการกำหนดเองใดๆ

#### <a name="salestransactionsignaturenorway-component"></a>ส่วนประกอบ SalesTransactionSignatureNorway

1. ค้นหาโครงการ **Runtime.Extensions.SalesTransactionSignatureNorway**
2. ในโฟลเดอร์ **Extensions.SalesTransactionSignatureNorway\\bin\\Debug** ให้ค้นหาไฟล์แอสเซมบลี **Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll**
3. คัดลอกไฟล์แอสเซมบลีไปยังโฟลเดอร์ส่วนขยาย CRT:

    - **เซิร์ฟเวอร์ระบบการขายปลีก:** คัดลอกแอสเซมบลีไปยังโฟลเดอร์ **\\bin\\ext** ภายใต้ที่ตั้งไซต์เซิร์ฟเวอร์ระบบการขายปลีกของ IIS
    - **CRT ท้องถิ่นบน POS สมัยใหม่:** คัดลอกแอสเซมบลีไปยังโฟลเดอร์ **\\ext** ภายใต้ที่ตั้งของ Client Broker ของ CRT ท้องถิ่น

4. ค้นหาไฟล์การกำหนดค่าส่วนขยายสำหรับ CRT:

    - **เซิร์ฟเวอร์ระบบการขายปลีก:** ไฟล์มีชื่อว่า **commerceruntime.ext.config** และอยู่ในโฟลเดอร์ **bin\\ext** ภายใต้ที่ตั้งไซต์เซิร์ฟเวอร์ระบบการขายปลีก IIS
    - **CRT เฉพาะที่บน Modern POS:** ไฟล์มีชื่อว่า **CommerceRuntime.MPOSOffline.Ext.config** และอยู่ภายใต้ที่ตั้ง Client Broker ของ CRT เฉพาะที่

5. ลงทะเบียนการเปลี่ยนแปลง CRT ในไฟล์การกำหนดค่าส่วนขยาย

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
    ```

    > [!WARNING]
    > ห้าม **ไม่ให้** แก้ไขไฟล์ commerceruntime.config และ CommerceRuntime.MPOSOffline.config ไฟล์เหล่านี้ไม่ได้มีไว้เพื่อการกำหนดเองใดๆ

#### <a name="sequentialsignatureregistercontracts-component"></a>ส่วนประกอบ SequentialSignatureRegister.Contracts

1. ค้นหาโครงการ **Runtime.Extensions.SequentialSignatureRegister.Contracts**
2. ในโฟลเดอร์ **Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug** ให้ค้นหาไฟล์แอสเซมบลี **Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll**
3. คัดลอกไฟล์แอสเซมบลีไปยังโฟลเดอร์ส่วนขยาย CRT:

    - **เซิร์ฟเวอร์ระบบการขายปลีก:** คัดลอกแอสเซมบลีไปยังโฟลเดอร์ **\\bin\\ext** ภายใต้ที่ตั้งไซต์เซิร์ฟเวอร์ระบบการขายปลีกของ IIS
    - **CRT ท้องถิ่นบน POS สมัยใหม่:** คัดลอกแอสเซมบลีไปยังโฟลเดอร์ **\\ext** ภายใต้ที่ตั้งของ Client Broker ของ CRT ท้องถิ่น

#### <a name="salespaymenttransextnorway-component"></a>ส่วนประกอบ SalesPaymentTransExtNorway

1. ค้นหาโครงการ **Runtime.Extensions.SalesPaymentTransExtNorway** และสร้าง
2. ในโฟลเดอร์ **Extensions.SalesPaymentTransExtNorway\\bin\\Debug** ให้ค้นหาไฟล์แอสเซมบลี **Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll**
3. คัดลอกไฟล์แอสเซมบลีไปยังโฟลเดอร์ส่วนขยาย CRT:

    - **เซิร์ฟเวอร์ระบบการขายปลีก:** คัดลอกแอสเซมบลีไปยังโฟลเดอร์ **\\bin\\ext** ภายใต้ที่ตั้งไซต์เซิร์ฟเวอร์ระบบการขายปลีกของ IIS
    - **CRT ท้องถิ่นบน POS สมัยใหม่:** คัดลอกแอสเซมบลีไปยังโฟลเดอร์ **\\ext** ภายใต้ที่ตั้งของ Client Broker ของ CRT ท้องถิ่น

4. ค้นหาไฟล์การกำหนดค่าส่วนขยายสำหรับ CRT:

    - **เซิร์ฟเวอร์ระบบการขายปลีก:** ไฟล์มีชื่อว่า **commerceruntime.ext.config** และอยู่ในโฟลเดอร์ **bin\\ext** ภายใต้ที่ตั้งไซต์เซิร์ฟเวอร์ระบบการขายปลีก IIS
    - **CRT เฉพาะที่บน Modern POS:** ไฟล์มีชื่อว่า **CommerceRuntime.MPOSOffline.Ext.config** และอยู่ภายใต้ที่ตั้ง Client Broker ของ CRT เฉพาะที่

5. ลงทะเบียนการเปลี่ยนแปลง CRT ในไฟล์การกำหนดค่าส่วนขยาย

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
    ```

    > [!WARNING]
    > ห้าม **ไม่ให้** แก้ไขไฟล์ commerceruntime.config และ CommerceRuntime.MPOSOffline.config ไฟล์เหล่านี้ไม่ได้มีไว้เพื่อการกำหนดเองใดๆ

# <a name="retail-811-and-later"></a>[Retail 8.1.1 และรุ่นที่ใหม่กว่า](#tab/retail-8-1-1)

#### <a name="registerauditeventnorway-component"></a>ส่วนประกอบ RegisterAuditEventNorway

1. ค้นหาไฟล์การกำหนดค่าส่วนขยายสำหรับ CRT:

    - **เซิร์ฟเวอร์ระบบการขายปลีก:** ไฟล์มีชื่อว่า **commerceruntime.ext.config** และอยู่ในโฟลเดอร์ **bin\\ext** ภายใต้ที่ตั้งไซต์เซิร์ฟเวอร์ระบบการขายปลีก IIS
    - **CRT เฉพาะที่บน Modern POS:** ไฟล์มีชื่อว่า **CommerceRuntime.MPOSOffline.Ext.config** และอยู่ภายใต้ที่ตั้ง Client Broker ของ CRT เฉพาะที่

2. ลงทะเบียนการเปลี่ยนแปลง CRT ในไฟล์การกำหนดค่าส่วนขยาย

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventNorway" />
    ```

    > [!WARNING]
    > ห้าม **ไม่ให้** แก้ไขไฟล์ commerceruntime.config และ CommerceRuntime.MPOSOffline.config ไฟล์เหล่านี้ไม่ได้มีไว้เพื่อการกำหนดเองใดๆ

#### <a name="sequentialsignatureregister-component"></a>ส่วนประกอบ SequentialSignatureRegister

1. ค้นหาโครงการ **Runtime.Extensions.SequentialSignatureRegister**
2. แก้ไขไฟล์ **App.config** โดยระบุรหัสประจำตัว ที่ตั้งร้านค้า และชื่อร้านค้าของใบรับรองที่ควรใช้ในการลงชื่อธุรกรรมการขาย
3. สร้างโครงการ
4. ในโฟลเดอร์ **Extensions.SequentialSignatureRegister\\bin\\Debug** ค้นหาไฟล์ต่อไปนี้:

    - ไฟล์แอสเซมบลี **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll**
    - ไฟล์การกำหนดค่า **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config**

5. คัดลอกไฟล์ไปยังโฟลเดอร์ส่วนขยาย CRT:

    - **เซิร์ฟเวอร์ระบบการขายปลีก:** คัดลอกแอสเซมบลีไปยังโฟลเดอร์ **\\bin\\ext** ภายใต้ที่ตั้งไซต์เซิร์ฟเวอร์ระบบการขายปลีกของ IIS
    - **CRT ท้องถิ่นบน POS สมัยใหม่:** คัดลอกแอสเซมบลีไปยังโฟลเดอร์ **\\ext** ภายใต้ที่ตั้งของ Client Broker ของ CRT ท้องถิ่น

6. ค้นหาไฟล์การกำหนดค่าส่วนขยายสำหรับ CRT:

    - **เซิร์ฟเวอร์ระบบการขายปลีก:** ไฟล์มีชื่อว่า **commerceruntime.ext.config** และอยู่ในโฟลเดอร์ **bin\\ext** ภายใต้ที่ตั้งไซต์เซิร์ฟเวอร์ระบบการขายปลีก IIS
    - **CRT เฉพาะที่บน Modern POS:** ไฟล์มีชื่อว่า **CommerceRuntime.MPOSOffline.Ext.config** และอยู่ภายใต้ที่ตั้ง Client Broker ของ CRT เฉพาะที่

7. ลงทะเบียนการเปลี่ยนแปลง CRT ในไฟล์การกำหนดค่าส่วนขยาย

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
    ```

    > [!WARNING]
    > ห้าม **ไม่ให้** แก้ไขไฟล์ commerceruntime.config และ CommerceRuntime.MPOSOffline.config ไฟล์เหล่านี้ไม่ได้มีไว้เพื่อการกำหนดเองใดๆ

#### <a name="salestransactionsignaturenorway-component"></a>ส่วนประกอบ SalesTransactionSignatureNorway

1. ค้นหาโครงการ **Runtime.Extensions.SalesTransactionSignatureNorway**
2. ในโฟลเดอร์ **Extensions.SalesTransactionSignatureNorway\\bin\\Debug** ให้ค้นหาไฟล์แอสเซมบลี **Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll**
3. คัดลอกไฟล์แอสเซมบลีไปยังโฟลเดอร์ส่วนขยาย CRT:

    - **เซิร์ฟเวอร์ระบบการขายปลีก:** คัดลอกแอสเซมบลีไปยังโฟลเดอร์ **\\bin\\ext** ภายใต้ที่ตั้งไซต์เซิร์ฟเวอร์ระบบการขายปลีกของ IIS
    - **CRT ท้องถิ่นบน POS สมัยใหม่:** คัดลอกแอสเซมบลีไปยังโฟลเดอร์ **\\ext** ภายใต้ที่ตั้งของ Client Broker ของ CRT ท้องถิ่น

4. ค้นหาไฟล์การกำหนดค่าส่วนขยายสำหรับ CRT:

    - **เซิร์ฟเวอร์ระบบการขายปลีก:** ไฟล์มีชื่อว่า **commerceruntime.ext.config** และอยู่ในโฟลเดอร์ **bin\\ext** ภายใต้ที่ตั้งไซต์เซิร์ฟเวอร์ระบบการขายปลีก IIS
    - **CRT เฉพาะที่บน Modern POS:** ไฟล์มีชื่อว่า **CommerceRuntime.MPOSOffline.Ext.config** และอยู่ภายใต้ที่ตั้ง Client Broker ของ CRT เฉพาะที่

5. ลงทะเบียนการเปลี่ยนแปลง CRT ในไฟล์การกำหนดค่าส่วนขยาย

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
    ```

    > [!WARNING]
    > ห้าม **ไม่ให้** แก้ไขไฟล์ commerceruntime.config และ CommerceRuntime.MPOSOffline.config ไฟล์เหล่านี้ไม่ได้มีไว้เพื่อการกำหนดเองใดๆ

#### <a name="sequentialsignatureregistercontracts-component"></a>ส่วนประกอบ SequentialSignatureRegister.Contracts

1. ค้นหาโครงการ **Runtime.Extensions.SequentialSignatureRegister.Contracts**
2. ในโฟลเดอร์ **Extensions.SequentialSignatureRegister.Contracts\\bin\\Debug** ให้ค้นหาไฟล์แอสเซมบลี **Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll**
3. คัดลอกไฟล์แอสเซมบลีไปยังโฟลเดอร์ส่วนขยาย CRT:

    - **เซิร์ฟเวอร์ระบบการขายปลีก:** คัดลอกแอสเซมบลีไปยังโฟลเดอร์ **\\bin\\ext** ภายใต้ที่ตั้งไซต์เซิร์ฟเวอร์ระบบการขายปลีกของ IIS
    - **CRT ท้องถิ่นบน POS สมัยใหม่:** คัดลอกแอสเซมบลีไปยังโฟลเดอร์ **\\ext** ภายใต้ที่ตั้งของ Client Broker ของ CRT ท้องถิ่น

#### <a name="salespaymenttransextnorway-component"></a>ส่วนประกอบ SalesPaymentTransExtNorway

1. ค้นหาโครงการ **Runtime.Extensions.SalesPaymentTransExtNorway** และสร้าง
2. ในโฟลเดอร์ **Extensions.SalesPaymentTransExtNorway\\bin\\Debug** ให้ค้นหาไฟล์แอสเซมบลี **Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll**
3. คัดลอกไฟล์แอสเซมบลีไปยังโฟลเดอร์ส่วนขยาย CRT:

    - **เซิร์ฟเวอร์ระบบการขายปลีก:** คัดลอกแอสเซมบลีไปยังโฟลเดอร์ **\\bin\\ext** ภายใต้ที่ตั้งไซต์เซิร์ฟเวอร์ระบบการขายปลีกของ IIS
    - **CRT ท้องถิ่นบน POS สมัยใหม่:** คัดลอกแอสเซมบลีไปยังโฟลเดอร์ **\\ext** ภายใต้ที่ตั้งของ Client Broker ของ CRT ท้องถิ่น

4. ค้นหาไฟล์การกำหนดค่าส่วนขยายสำหรับ CRT:

    - **เซิร์ฟเวอร์ระบบการขายปลีก:** ไฟล์มีชื่อว่า **commerceruntime.ext.config** และอยู่ในโฟลเดอร์ **bin\\ext** ภายใต้ที่ตั้งไซต์เซิร์ฟเวอร์ระบบการขายปลีก IIS
    - **CRT เฉพาะที่บน Modern POS:** ไฟล์มีชื่อว่า **CommerceRuntime.MPOSOffline.Ext.config** และอยู่ภายใต้ที่ตั้ง Client Broker ของ CRT เฉพาะที่

5. ลงทะเบียนการเปลี่ยนแปลง CRT ในไฟล์การกำหนดค่าส่วนขยาย

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
    ```

    > [!WARNING]
    > ห้าม **ไม่ให้** แก้ไขไฟล์ commerceruntime.config และ CommerceRuntime.MPOSOffline.config ไฟล์เหล่านี้ไม่ได้มีไว้เพื่อการกำหนดเองใดๆ

---

### <a name="the-retail-server-extension-components"></a>ส่วนประกอบของส่วนขยายเซิร์ฟเวอร์ระบบการขายปลีก

#### <a name="salestransactionsignature-retail-server-sample-component"></a>ส่วนประกอบตัวอย่างเซิร์ฟเวอร์ระบบการขายปลีก SalesTransactionSignature

1. ในโฟลเดอร์ **RetailSDK\\SampleExtensions\\RetailServer\\RetailServer.Extensions.SalesTransactionSignatureSample** ให้ค้นหาโครงการ **RetailServer.Extensions.SalesTransactionSignatureSample** และสร้าง
2. ในโฟลเดอร์ **RetailServer\\Extensions.SalesTransactionSignatureSample\\bin\\Debug** ให้ค้นหาไฟล์แอสเซมบลี **Contoso.RetailServer.SalesTransactionSignatureSample.dll**
3. คัดลอกไฟล์แอสเซมบลีไปยังโฟลเดอร์ส่วนขยายของเซิร์ฟเวอร์ระบบการขายปลีก

    # <a name="application-update-4"></a>[Application update 4](#tab/app-update-4)

    โฟลเดอร์คือโฟลเดอร์ **\\bin** ภายใต้ที่ตั้งของไซต์เซิร์ฟเวอร์ระบบการขายปลีก IIS

    # <a name="application-update-5-and-later"></a>[Application update 5 และรุ่นใหม่กว่า](#tab/app-update-5-and-later)

    โฟลเดอร์คือโฟลเดอร์ **\\bin** ภายใต้ที่ตั้งของไซต์เซิร์ฟเวอร์ระบบการขายปลีก IIS

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    โฟลเดอร์คือโฟลเดอร์ **\\bin\\ext** ภายใต้ที่ตั้งของไซต์เซิร์ฟเวอร์ระบบการขายปลีก IIS

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 และรุ่นที่ใหม่กว่า](#tab/retail-7-3-2)

    โฟลเดอร์คือโฟลเดอร์ **\\bin\\ext** ภายใต้ที่ตั้งของไซต์เซิร์ฟเวอร์ระบบการขายปลีก IIS

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 และรุ่นที่ใหม่กว่า](#tab/retail-7-3-5)

    โฟลเดอร์คือโฟลเดอร์ **\\bin\\ext** ภายใต้ที่ตั้งของไซต์เซิร์ฟเวอร์ระบบการขายปลีก IIS

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 และรุ่นที่ใหม่กว่า](#tab/retail-8-1-1)

    โฟลเดอร์คือโฟลเดอร์ **\\bin\\ext** ภายใต้ที่ตั้งของไซต์เซิร์ฟเวอร์ระบบการขายปลีก IIS

    ---

4. ค้นหาไฟล์การกำหนดค่าจากเซิร์ฟเวอร์ระบบการขายปลีก ไฟล์มีชื่อว่า **web.config** และอยู่ในโฟลเดอร์รากภายใต้ที่ตั้งไซต์เซิร์ฟเวอร์ระบบการขายปลีก IIS
5. ลงทะเบียนส่วนขยายของเซิร์ฟเวอร์ระบบการขายปลีกในส่วน **extensionComposition** ของไฟล์การกำหนดค่า

    ``` xml
    <add source="assembly" value="Contoso.RetailServer.SalesTransactionSignatureSample" />
    ```

6. ลงทะเบียนการขึ้นต่อกันของส่วนขยายของเซิร์ฟเวอร์ระบบการขายปลีก

    # <a name="application-update-4"></a>[Application update 4](#tab/app-update-4/)

    1. ในโฟลเดอร์ **CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\bin\\Debug** ค้นหาไฟล์ต่อไปนี้:

        - ไฟล์แอสเซมบลี **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll**
        - ไฟล์การกำหนดค่า **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config**

    2. คัดลอกไฟล์ไปยังโฟลเดอร์ **\\bin** ภายใต้ที่ตั้งของไซต์เซิร์ฟเวอร์ระบบการขายปลีก IIS
    3. ลงทะเบียนการเปลี่ยนแปลง CRT ในไฟล์การกำหนดค่านามสกุลของ CRT ไฟล์นี้มีชื่อว่า **commerceruntime.ext.config** และอยู่ในโฟลเดอร์ **bin** ภายใต้ที่ตั้งไซต์เซิร์ฟเวอร์ระบบการขายปลีก IIS

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
        ```

    # <a name="application-update-5-and-later"></a>[Application update 5 และรุ่นใหม่กว่า](#tab/app-update-5-and-later/)

    1. ในโฟลเดอร์ **CommerceRuntime\\Extensions.SalesTransactionSignatureSample.Messages\\bin\\Debug** ให้ค้นหาไฟล์แอสเซมบลี **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages.dll**
    2. คัดลอกไฟล์ไปยังโฟลเดอร์ **\\bin** ภายใต้ที่ตั้งของไซต์เซิร์ฟเวอร์ระบบการขายปลีก IIS
    3. ลงทะเบียนการเปลี่ยนแปลง CRT ในไฟล์การกำหนดค่านามสกุลของ CRT ไฟล์นี้มีชื่อว่า **commerceruntime.ext.config** และอยู่ในโฟลเดอร์ **bin** ภายใต้ที่ตั้งไซต์เซิร์ฟเวอร์ระบบการขายปลีก IIS

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages" />
        ```

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    > [!NOTE]
    > ไม่จำเป็นต้องใช้การดำเนินการ

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 และรุ่นที่ใหม่กว่า](#tab/retail-7-3-2)

    > [!NOTE]
    > ไม่จำเป็นต้องใช้การดำเนินการ

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 และรุ่นที่ใหม่กว่า](#tab/retail-7-3-5)

    > [!NOTE]
    > ไม่จำเป็นต้องใช้การดำเนินการ

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 และรุ่นที่ใหม่กว่า](#tab/retail-8-1-1)

    > [!NOTE]
    > ไม่จำเป็นต้องใช้การดำเนินการ

    ---

### <a name="the-modern-pos-extension-components"></a>ส่วนประกอบส่วนขยาย POS สมัยใหม่

#### <a name="implement-the-proxy-code-for-offline-mode"></a>ใช้รหัสพร็อกซีเป็นโหมดออฟไลน์

ส่วนนี้จะเทียบเท่ากับตัวควบคุมเซิร์ฟเวอร์ระบบการขายปลีก แต่ขยาย CRT ท้องถิ่นที่ใช้เมื่อไคลเอ็นต์ไม่ได้เชื่อมต่อ

1. ในไฟล์ **customization.settings** ให้เปลี่ยนส่วน **@(RetailServerLibraryPathForProxyGeneration)** เพื่อให้ใช้แอสเซมบลีเซิร์ฟเวอร์ระบบการขายปลีกใหม่ในการสร้างพร็อกซี
2. ใช้วิธีการอินเทอร์เฟสต่อไปนี้ในคลาส **StoreOperationsManager** สำหรับการเกิดซ้ำครั้งแรก เพิ่มรหัสต่อไปนี้:

    # <a name="application-update-4"></a>[Application update 4](#tab/app-update-4)

    ``` csharp
    public Task<bool> SalesTransactionSignatureServiceIsReady()
    {
        throw new NotImplementedException();
    }
    public Task<FiscalTransaction> GetLastFiscalTransaction(string storeNumber, string terminalId)
    {
        throw new NotImplementedException();
    }
    ```

    # <a name="application-update-5-and-later"></a>[Application update 5 และรุ่นใหม่กว่า](#tab/app-update-5-and-later)

    ``` csharp
    public Task<bool> SalesTransactionSignatureServiceIsReady(string correlationId)
    {
        throw new NotImplementedException();
    }
    public Task<FiscalTransaction> GetLastFiscalTransaction(string storeNumber, string terminalId)
    {
        throw new NotImplementedException();
    }
    ```

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    > [!NOTE]
    > ขั้นตอนนี้ใช้กับรุ่นนี้

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 และรุ่นที่ใหม่กว่า](#tab/retail-7-3-2)

    > [!NOTE]
    > ขั้นตอนนี้ใช้กับรุ่นนี้

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 และรุ่นที่ใหม่กว่า](#tab/retail-7-3-5)

    > [!NOTE]
    > ขั้นตอนนี้ใช้กับรุ่นนี้

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 และรุ่นที่ใหม่กว่า](#tab/retail-8-1-1)

    > [!NOTE]
    > ขั้นตอนนี้ใช้กับรุ่นนี้

    ---

3. เมื่อต้องการสร้างรหัสพร็อกซีใหม่ ให้สร้างโฟลเดอร์ **พร็อกซี** จากบรรทัดคำสั่งโดยใช้คำสั่ง **msbuild /t:Rebuild**
4. แก้ไขความเชื่อมโยงโครงการ **Proxies.RetailProxy**:

    # <a name="application-update-4"></a>[Application update 4](#tab/app-update-4)

    เปิด **RetailSDK\\Proxies\\RetailProxy\\Proxies.RetailProxy.csproj** เพิ่มโครงการ **RetailSDK\\SampleExtensions\\CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\CommerceRuntime.Extensions.SalesTransactionSignatureSample** ไปยังโซลูชันและเพิ่มการอ้างอิงโครงการไปยังโครงการ **RetailProxy** เพื่ออ้างอิง **SalesTransactionSignatureSample**

    # <a name="application-update-5-and-later"></a>[Application update 5 และรุ่นใหม่กว่า](#tab/app-update-5-and-later)

    เปิด **RetailSDK\\Proxies\\RetailProxy\\Proxies.RetailProxy.csproj** เพิ่มโครงการ **RetailSDK\\SampleExtensions\\CommerceRuntime\\Extensions.SalesTransactionSignatureSample.Messages\\CommerceRuntime.Extensions.SalesTransactionSignatureSample.Messages** ไปยังโซลูชันและเพิ่มการอ้างอิงโครงการไปยังโครงการ **RetailProxy** เพื่ออ้างอิง **SalesTransactionSignatureSample**

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    > [!NOTE]
    > ขั้นตอนนี้ใช้กับรุ่นนี้

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 และรุ่นที่ใหม่กว่า](#tab/retail-7-3-2)

    > [!NOTE]
    > ขั้นตอนนี้ใช้กับรุ่นนี้

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 และรุ่นที่ใหม่กว่า](#tab/retail-7-3-5)

    > [!NOTE]
    > ขั้นตอนนี้ใช้กับรุ่นนี้

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 และรุ่นที่ใหม่กว่า](#tab/retail-8-1-1)

    > [!NOTE]
    > ขั้นตอนนี้ใช้กับรุ่นนี้

    ---

5. ปรับปรุงวิธีการอินเทอร์เฟสในคลาส **StoreOperationsManager**:

    # <a name="application-update-4"></a>[Application update 4](#tab/app-update-4)

    ``` csharp
    public Task<bool> SalesTransactionSignatureServiceIsReady()
    {
        return Task.Run(() => CommerceRuntimeManager.Runtime.Execute<SalesTransactionSignatureServiceIsReadyResponse>(new SalesTransactionSignatureServiceIsReadyRequest(), null).IsReady);
    }
    public Task<FiscalTransaction> GetLastFiscalTransaction(string storeNumber, string terminalId)
    {
        return Task.Run(() => CommerceRuntimeManager.Runtime.Execute<GetLastFiscalTransactionResponse>(new GetLastFiscalTransactionRequest(), null).FiscalTransaction);
    }
    ```

    # <a name="application-update-5-and-later"></a>[Application update 5 และรุ่นใหม่กว่า](#tab/app-update-5-and-later)

    ``` csharp
    public Task<bool> SalesTransactionSignatureServiceIsReady(string correlationId)
    {
        return Task.Run(() => CommerceRuntimeManager.Runtime.Execute<SalesTransactionSignatureServiceIsReadyResponse>(new SalesTransactionSignatureServiceIsReadyRequest(), null).IsReady);
    }
    public Task<FiscalTransaction> GetLastFiscalTransaction(string storeNumber, string terminalId)
    {
        return Task.Run(() => CommerceRuntimeManager.Runtime.Execute<GetLastFiscalTransactionResponse>(new GetLastFiscalTransactionRequest(), null).FiscalTransaction);
    }
    ```

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    > [!NOTE]
    > ขั้นตอนนี้ใช้กับรุ่นนี้

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 และรุ่นที่ใหม่กว่า](#tab/retail-7-3-2)

    > [!NOTE]
    > ขั้นตอนนี้ใช้กับรุ่นนี้

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 และรุ่นที่ใหม่กว่า](#tab/retail-7-3-5)

    > [!NOTE]
    > ขั้นตอนนี้ใช้กับรุ่นนี้

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 และรุ่นที่ใหม่กว่า](#tab/retail-8-1-1)

    > [!NOTE]
    > ขั้นตอนนี้ใช้กับรุ่นนี้

    ---

6. อัปเดตไฟล์ **dllhost.exe.config** เพื่อให้นา Client Broker โหลดแอสเซมบลี RetailProxy ใหม่

    ``` xml
    <add key="RetailProxyAssemblyName" value="Contoso.Commerce.RetailProxy" />
    <add key="AdaptorCallerFullTypeName" value="Contoso.Commerce.RetailProxy.Adapters.AdaptorCaller" />
    ```

#### <a name="retail-proxy-extension-component-retail-731-and-later"></a>ส่วนประกอบส่วนขยายของพร็อกซีการขายปลีก (Retail 7.3.1 และรุ่นที่ใหม่กว่า)

ปฏิบัติตามขั้นตอนต่อไปนี้ให้เสร็จสมบูรณ์เฉพาะเมื่อคุณใช้ Retail 7.3.1 และรุ่นที่ใหม่กว่า

1. ในโฟลเดอร์ **RetailSDK\\SampleExtensions\\RetailProxy\\RetailProxy.Extensions.SalesTransactionSignatureSample** ให้ค้นหาโครงการ **RetailServer.Extensions.SalesTransactionSignatureSample** และสร้าง
2. ในโฟลเดอร์ **RetailProxy\\RetailProxy.Extensions.SalesTransactionSignatureSample\\bin\\Debug** ให้ค้นหาไฟล์แอสเซมบลี **Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample**
3. คัดลอกไฟล์แอสเซมบลีไปยังโฟลเดอร์ **\\ext** ภายใต้ที่ตั้งของ Client Broker ของ CRT ท้องถิ่น
4. ลงทะเบียนการเปลี่ยนแปลงพร็อกซีการขายปลีกในไฟล์การกำหนดค่านามสกุล มีการตั้งชื่อไฟล์เป็น **RetailProxy.MPOSOffline.ext.config** และอยู่ภายใต้ที่ตั้งของ Client Broker ของ CRT ท้องถิ่น

    ``` xml
    <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
    ```

#### <a name="modern-pos-extension-components"></a>ส่วนประกอบส่วนขยาย POS สมัยใหม่

1. เปิดโซลูชันที่ **RetailSdk\\POS\\ModernPOS.sln** และตรวจสอบให้แน่ใจว่าโซลูชันนั้นสามารถคอมไพล์ได้โดยไม่มีข้อผิดพลาด นอกจากนี้ ให้ตรวจสอบให้แน่ใจว่าคุณสามารถรัน POS สมัยใหม่จาก Microsoft Visual Studio ได้โดยใช้คำสั่ง **Run**

    > [!NOTE]
    > POS สมัยใหม่ต้องไม่กำหนดเอง คุณต้องเปิดใช้งานการควบคุมบัญชีผู้ใช้ (UAC) และคุณต้องถอนการติดตั้งอินสแตนซ์ของ POS สมัยใหม่ที่ติดตั้งไว้ก่อนหน้านี้ตามที่ต้องการ

2. รวมโฟลเดอร์รหัสต้นทางที่มีอยู่ต่อไปนี้ในโครงการ **Pos.Extensions**

    # <a name="application-update-4"></a>[Application update 4](#tab/app-update-4)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="application-update-5-and-later"></a>[Application update 5 และรุ่นใหม่กว่า](#tab/app-update-5-and-later)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 และรุ่นที่ใหม่กว่า](#tab/retail-7-3-2)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 และรุ่นที่ใหม่กว่า](#tab/retail-7-3-5)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 และรุ่นที่ใหม่กว่า](#tab/retail-8-1-1)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    ---

3. เปิดใช้งานส่วนขยายที่จะคอมไพล์ใน **tsconfig.json** โดยการลบโฟลเดอร์ต่อไปนี้ออกจากรายการแยก

    # <a name="application-update-4"></a>[Application update 4](#tab/app-update-4)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="application-update-5-and-later"></a>[Application update 5 และรุ่นใหม่กว่า](#tab/app-update-5-and-later)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 และรุ่นที่ใหม่กว่า](#tab/retail-7-3-2)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 และรุ่นที่ใหม่กว่า](#tab/retail-7-3-5)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 และรุ่นที่ใหม่กว่า](#tab/retail-8-1-1)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    ---

4. เปิดใช้งานส่วนขยายที่จะโหลดใน **extensions.json** โดยการเพิ่มบรรทัดต่อไปนี้ในที่ที่เหมาะสม

    # <a name="application-update-4"></a>[Application update 4](#tab/app-update-4)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="application-update-5-and-later"></a>[Application update 5 และรุ่นใหม่กว่า](#tab/app-update-5-and-later)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 และรุ่นที่ใหม่กว่า](#tab/retail-7-3-2)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 และรุ่นที่ใหม่กว่า](#tab/retail-7-3-5)

    ``` json
    {
        "baseUrl": "Microsoft/AuditEvent.NO"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 และรุ่นที่ใหม่กว่า](#tab/retail-8-1-1)

    ``` json
    {
        "baseUrl": "Microsoft/AuditEvent.NO"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    ---

    > [!NOTE]
    > สำหรับข้อมูลเพิ่มเติม และตัวอย่างที่แสดงวิธีการรวมโฟลเดอร์รหัสต้นฉบับและเปิดใช้งานส่วนขยายที่จะโหลด โปรดดูคําแนะนําในไฟล์ readme.md ในโครงการ **Pos.Extensions**

5. สร้างโซลูชันใหม่
6. เรียกใช้ POS สมัยใหม่ในดีบักเกอร์ และทดสอบฟังก์ชัน

### <a name="cloud-pos-extension-components"></a>ส่วนประกอบส่วนขยาย POS ระบบคลาวด์

1. เปิดโซลูชันที่ **RetailSdk\\POS\\CloudPOS.sln** และตรวจสอบให้แน่ใจว่าโซลูชันนั้นสามารถคอมไพล์ได้โดยไม่มีข้อผิดพลาด
2. รวมโฟลเดอร์รหัสต้นทางที่มีอยู่ต่อไปนี้ในโครงการ **Pos.Extensions**

    # <a name="application-update-4"></a>[Application update 4](#tab/app-update-4)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="application-update-5-and-later"></a>[Application update 5 และรุ่นใหม่กว่า](#tab/app-update-5-and-later)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 และรุ่นที่ใหม่กว่า](#tab/retail-7-3-2)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 และรุ่นที่ใหม่กว่า](#tab/retail-7-3-5)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 และรุ่นที่ใหม่กว่า](#tab/retail-8-1-1)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    ---

3. เปิดใช้งานส่วนขยายที่จะคอมไพล์ใน **tsconfig.json** โดยการลบโฟลเดอร์ต่อไปนี้ออกจากรายการแยก

    # <a name="application-update-4"></a>[Application update 4](#tab/app-update-4)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="application-update-5-and-later"></a>[Application update 5 และรุ่นใหม่กว่า](#tab/app-update-5-and-later)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 และรุ่นที่ใหม่กว่า](#tab/retail-7-3-2)

    - AuditEventExtensionSample
    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 และรุ่นที่ใหม่กว่า](#tab/retail-7-3-5)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 และรุ่นที่ใหม่กว่า](#tab/retail-8-1-1)

    - SalesTransactionSignatureSample
    - SalesTransactionSignatureNorway
    - SequentialSignature

    ---

4. เปิดใช้งานส่วนขยายที่จะโหลดใน **extensions.json** โดยการเพิ่มบรรทัดต่อไปนี้ในที่ที่เหมาะสม

    # <a name="application-update-4"></a>[Application update 4](#tab/app-update-4)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="application-update-5-and-later"></a>[Application update 5 และรุ่นใหม่กว่า](#tab/app-update-5-and-later)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    }
    ```

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 และรุ่นที่ใหม่กว่า](#tab/retail-7-3-2)

    ``` json
    {
        "baseUrl": "AuditEventExtensionSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 และรุ่นที่ใหม่กว่า](#tab/retail-7-3-5)

    ``` json
    {
        "baseUrl": "Microsoft/AuditEvent.NO"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 และรุ่นที่ใหม่กว่า](#tab/retail-8-1-1)

    ``` json
    {
        "baseUrl": "Microsoft/AuditEvent.NO"
    },
    {
        "baseUrl": "SalesTransactionSignatureSample"
    },
    {
        "baseUrl": "SalesTransactionSignatureNorway"
    },
    {
        "baseUrl": "SequentialSignature"
    }
    ```

    ---

    > [!NOTE]
    > สำหรับข้อมูลเพิ่มเติม และตัวอย่างที่แสดงวิธีการรวมโฟลเดอร์รหัสต้นฉบับและเปิดใช้งานส่วนขยายที่จะโหลด โปรดดูคําแนะนําในไฟล์ readme.md ในโครงการ **Pos.Extensions**

5. สร้างโซลูชันใหม่
6. เรียกใช้โซลูชันโดยใช้คำสั่ง **Run** และปฏิบัติตามขั้นตอนในคู่มือ Retail SDK
7. ทดสอบฟังก์ชัน

### <a name="set-up-required-parameters-in-headquarters"></a>ตั้งค่าพารามิเตอร์ที่จำเป็นในศูนย์ควบคุม

สำหรับข้อมูลเพิ่มเติม ดู [ฟังก์ชันเครื่องบันทึกเงินสดสำหรับนอร์เวย์](./emea-nor-cash-registers.md)

## <a name="production-environment"></a>สภาพแวดล้อมการทำงานจริง

ปฏิบัติตามขั้นตอนต่อไปนี้เพื่อสร้างแพคเกจที่สามารถปรับใช้ได้ซึ่งมีส่วนประกอบของ Commerce และเพื่อใช้แพคเกจเหล่านั้นในสภาพแวดล้อมการทำงานจริง

1. ปฏิบัติตามขั้นตอนต่างๆ ในส่วน [ส่วนประกอบของส่วนขยาย Cloud POS](#cloud-pos-extension-components) หรือ [ส่วนประกอบของส่วนขยาย POS สมัยใหม่](#modern-pos-extension-components) ที่อธิบายไว้ก่อนหน้านี้ในบทความนี้
2. ทำการเปลี่ยนแปลงต่อไปนี้ในไฟล์การตั้งค่าคอนฟิกแพคเกจภายใต้โฟลเดอร์ **RetailSdk\\Assets**:

    1. ในไฟล์การกำหนดค่า **commerceruntime.ext.config** และ **CommerceRuntime.MPOSOffline.Ext.config** ให้เพิ่มรายการต่อไปนี้ลงในส่วน **องค์ประกอบ**:

        # <a name="application-update-4"></a>[Application update 4](#tab/app-update-4)

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="application-update-5-and-later"></a>[Application update 5 และรุ่นใหม่กว่า](#tab/app-update-5-and-later)

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="retail-732-and-later"></a>[Retail 7.3.2 และรุ่นที่ใหม่กว่า](#tab/retail-7-3-2)

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="retail-735-and-later"></a>[Retail 7.3.5 และรุ่นที่ใหม่กว่า](#tab/retail-7-3-5)

        ``` xml
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.RegisterAuditEventSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        # <a name="retail-811-and-later"></a>[Retail 8.1.1 และรุ่นที่ใหม่กว่า](#tab/retail-8-1-1)

        ``` xml
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExt" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesPaymentTransExtNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SequentialSignatureRegister" />
        <add source="assembly" value="Contoso.Commerce.Runtime.SalesTransactionSignatureNorway" />
        <add source="assembly" value="Contoso.Commerce.Runtime.XZReportsNorway" />
        ```

        ---

    2. เปิดใช้งานการกำหนดเองของพร็อกซี Commerce:

        # <a name="application-update-4"></a>[Application update 4](#tab/app-update-4)

        ในไฟล์การกำหนดค่า **dllhost.exe.config** ให้เพิ่มรายการต่อไปนี้ลงในส่วนย่อย **appSettings** ของส่วน **การกำหนดค่า**

        ``` xml
        <add key="RetailProxyAssemblyName" value="Contoso.Commerce.RetailProxy"/>
        <add key="AdaptorCallerFullTypeName" value ="Contoso.Commerce.RetailProxy.Adapters.AdaptorCaller"/>
        ```

        # <a name="application-update-5-and-later"></a>[Application update 5 และรุ่นใหม่กว่า](#tab/app-update-5-and-later)

        ในไฟล์การกำหนดค่า **dllhost.exe.config** ให้เพิ่มรายการต่อไปนี้ลงในส่วนย่อย **appSettings** ของส่วน **การกำหนดค่า**

        ``` xml
        <add key="RetailProxyAssemblyName" value="Contoso.Commerce.RetailProxy"/>
        <add key="AdaptorCallerFullTypeName" value ="Contoso.Commerce.RetailProxy.Adapters.AdaptorCaller"/>
        ```

        # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

        ในไฟล์การกำหนดค่า **RetailProxy.MPOSOffline.ext.config** ให้เพิ่มรายการต่อไปนี้ในส่วน **องค์ประกอบ**:

        ``` xml
        <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
        ```

        # <a name="retail-732-and-later"></a>[Retail 7.3.2 และรุ่นที่ใหม่กว่า](#tab/retail-7-3-2)

        ในไฟล์การกำหนดค่า **RetailProxy.MPOSOffline.ext.config** ให้เพิ่มรายการต่อไปนี้ในส่วน **องค์ประกอบ**:

        ``` xml
        <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
        ```

        # <a name="retail-735-and-later"></a>[Retail 7.3.5 และรุ่นที่ใหม่กว่า](#tab/retail-7-3-5)

        ในไฟล์การกำหนดค่า **RetailProxy.MPOSOffline.ext.config** ให้เพิ่มรายการต่อไปนี้ในส่วน **องค์ประกอบ**:

        ``` xml
        <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
        ```

        # <a name="retail-811-and-later"></a>[Retail 8.1.1 และรุ่นที่ใหม่กว่า](#tab/retail-8-1-1)

        ในไฟล์การกำหนดค่า **RetailProxy.MPOSOffline.ext.config** ให้เพิ่มรายการต่อไปนี้ในส่วน **องค์ประกอบ**:

        ``` xml
        <add source="assembly" value="Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample" />
        ```

        ---

3. การเปลี่ยนแปลงต่อไปนี้ในไฟล์การกำหนดค่าการกําหนดเองของแพคเกจ **Customization.settings**:

    1. เปิดใช้งานการกำหนดเองของพร็อกซี Retail

        # <a name="application-update-4"></a>[Application update 4](#tab/app-update-4)

        เพิ่มรายการต่อไปนี้ลงในส่วน **&lt;ItemGroup Condition="'@(RetailServerLibraryPathForProxyGeneration)' == ''"&gt;**

        ``` xml
        <RetailServerLibraryPathForProxyGeneration Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll"/>
        ```

        # <a name="application-update-5-and-later"></a>[Application update 5 และรุ่นใหม่กว่า](#tab/app-update-5-and-later)

        เพิ่มรายการต่อไปนี้ลงในส่วน **&lt;ItemGroup Condition="'@(RetailServerLibraryPathForProxyGeneration)' == ''"&gt;**

        ``` xml
        <RetailServerLibraryPathForProxyGeneration Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll"/>
        ```

        # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

        เพิ่มรายการต่อไปนี้ลงในส่วน **ItemGroup** เพื่อรวมส่วนขยายพร็อกซีของ Retail ในแพคเกจที่สามารถปรับใช้ได้:

        ``` xml
        <ISV_RetailProxy_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-732-and-later"></a>[Retail 7.3.2 และรุ่นที่ใหม่กว่า](#tab/retail-7-3-2)

        เพิ่มรายการต่อไปนี้ลงในส่วน **ItemGroup** เพื่อรวมส่วนขยายพร็อกซีของ Retail ในแพคเกจที่สามารถปรับใช้ได้:

        ``` xml
        <ISV_RetailProxy_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-735-and-later"></a>[Retail 7.3.5 และรุ่นที่ใหม่กว่า](#tab/retail-7-3-5)

        เพิ่มรายการต่อไปนี้ลงในส่วน **ItemGroup** เพื่อรวมส่วนขยายพร็อกซีของ Retail ในแพคเกจที่สามารถปรับใช้ได้:

        ``` xml
        <ISV_RetailProxy_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-811-and-later"></a>[Retail 8.1.1 และรุ่นที่ใหม่กว่า](#tab/retail-8-1-1)

        เพิ่มรายการต่อไปนี้ลงในส่วน **ItemGroup** เพื่อรวมส่วนขยายพร็อกซีของ Retail ในแพคเกจที่สามารถปรับใช้ได้:

        ``` xml
        <ISV_RetailProxy_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.RetailProxy.SalesTransactionSignatureSample.dll" />
        ```

        ---

    2. เพิ่มรายการต่อไปนี้ลงในส่วน **ItemGroup** เพื่อรวมส่วนขยาย CRT ในแพคเกจที่สามารถปรับใช้ได้:

        # <a name="application-update-4"></a>[Application update 4](#tab/app-update-4)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.RegisterAuditEventSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="application-update-5-and-later"></a>[Application update 5 และรุ่นใหม่กว่า](#tab/app-update-5-and-later)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.RegisterAuditEventSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.RegisterAuditEventSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="retail-732-and-later"></a>[Retail 7.3.2 และรุ่นที่ใหม่กว่า](#tab/retail-7-3-2)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.RegisterAuditEventSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="retail-735-and-later"></a>[Retail 7.3.5 และรุ่นที่ใหม่กว่า](#tab/retail-7-3-5)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        # <a name="retail-811-and-later"></a>[Retail 8.1.1 และรุ่นที่ใหม่กว่า](#tab/retail-8-1-1)

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.ReceiptsNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExt.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesPaymentTransExtNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureNorway.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SequentialSignatureRegister.Contracts.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.XZReportsNorway.dll" />
        ```

        ---

    3. เพิ่มรายการต่อไปนี้ลงในส่วน **ItemGroup** เพื่อรวมส่วนขยายพร็อกซีของ Retail Server ในแพคเกจที่สามารถปรับใช้ได้:

        # <a name="application-update-4"></a>[Application update 4](#tab/app-update-4)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll" />
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config" />
        ```

        # <a name="application-update-5-and-later"></a>[Application update 5 และรุ่นใหม่กว่า](#tab/app-update-5-and-later)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.SalesTransactionSignatureSample.Messages.dll" />
        ```

        # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-732-and-later"></a>[Retail 7.3.2 และรุ่นที่ใหม่กว่า](#tab/retail-7-3-2)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-735-and-later"></a>[Retail 7.3.5 และรุ่นที่ใหม่กว่า](#tab/retail-7-3-5)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        ```

        # <a name="retail-811-and-later"></a>[Retail 8.1.1 และรุ่นที่ใหม่กว่า](#tab/retail-8-1-1)

        ``` xml
        <ISV_RetailServer_CustomizableFile Include="$(SdkReferencesPath)\Contoso.RetailServer.SalesTransactionSignatureSample.dll" />
        ```

        ---

4. แก้ไขไฟล์ต่อไปนี้เพื่อรวมไฟล์ทรัพยากรสำหรับนอร์เวย์ในแพคเกจที่สามารถปรับใช้ได้:
    - Packages\_SharedPackagingProjectComponents\Sdk.ModernPos.Shared.csproj
    - Packages\RetailServer\Sdk.RetailServerSetup.proj
  
  - สำหรับไฟล์ **Sdk.ModernPos.Shared.csproj** 
    - เพิ่มรายการลงในส่วน **ItemGroup**
    
        ``` xml
        <<File_name> Include="$(SdkReferencesPath)\nb-NO\*" />
        ```
    > [!Note]
    > แทน <File_name> ที่ระบุชื่อของไฟล์ทรัพยากร ข้อมูลเดียวกันนี้จะเกี่ยวข้องกับตัวอย่างอื่นๆ ที่ข้างล่างนี้
 
    - เพิ่มรายการลงในส่วน **ชื่อเป้าหมาย="CopyPackageFiles"**
       ``` xml
        <Copy SourceFiles="@(<File_name>)" DestinationFolder="$(OutputPath)content.folder\CustomizedFiles\ClientBroker\ext\nb-NO" SkipUnchangedFiles="true" />
        ```
  
  - สำหรับไฟล์ **Sdk.RetailServerSetup.proj** 
    - เพิ่มรายการลงในส่วน **ItemGroup**
        ``` xml
        <<File_name> Include="$(SdkReferencesPath)\nb-NO\*" />
        ```    
    - เพิ่มรายการลงในส่วน **ชื่อเป้าหมาย="CopyPackageFiles"**
         ``` xml
        <Copy SourceFiles="@(<File_name>)" DestinationFolder="$(OutputPath)content.folder\RetailServer\Code\bin\ext\nb-NO" SkipUnchangedFiles="true" />
        ```    

5. แก้ไขไฟล์การกำหนดค่าของใบรับรองโดยระบุรหัสประจำตัว ที่ตั้งร้านค้า และชื่อร้านค้าของใบรับรองที่ควรใช้ในการลงชื่อธุรกรรมการขาย จากนั้นคัดลอกไฟล์การกำหนดค่าไปยังโฟลเดอร์ **การอ้างอิง**

    # <a name="application-update-4"></a>[Application update 4](#tab/app-update-4)

    มีการตั้งชื่อไฟล์เป็น **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** และอยู่ใต้ **CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\bin\\Debug**

    # <a name="application-update-5-and-later"></a>[Application update 5 และรุ่นใหม่กว่า](#tab/app-update-5-and-later)

    มีการตั้งชื่อไฟล์เป็น **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** และอยู่ใต้ **CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\bin\\Debug**

    # <a name="retail-731"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    มีการตั้งชื่อไฟล์เป็น **Contoso.Commerce.Runtime.SalesTransactionSignatureSample.dll.config** และอยู่ใต้ **CommerceRuntime\\Extensions.SalesTransactionSignatureSample\\bin\\Debug**

    # <a name="retail-732-and-later"></a>[Retail 7.3.2 และรุ่นที่ใหม่กว่า](#tab/retail-7-3-2)

    มีการตั้งชื่อไฟล์เป็น **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** และอยู่ใต้ **Extensions.SequentialSignatureRegister\\bin\\Debug**

    # <a name="retail-735-and-later"></a>[Retail 7.3.5 และรุ่นที่ใหม่กว่า](#tab/retail-7-3-5)

    มีการตั้งชื่อไฟล์เป็น **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** และอยู่ใต้ **Extensions.SequentialSignatureRegister\\bin\\Debug**

    # <a name="retail-811-and-later"></a>[Retail 8.1.1 และรุ่นที่ใหม่กว่า](#tab/retail-8-1-1)

    มีการตั้งชื่อไฟล์เป็น **Contoso.Commerce.Runtime.SequentialSignatureRegister.dll.config** และอยู่ใต้ **Extensions.SequentialSignatureRegister\\bin\\Debug**

    ---

6. อัปเดตไฟล์การกำหนดค่าจากเซิร์ฟเวอร์ระบบการขายปลีก ในไฟล์ **RetailSDK\\Packages\\RetailServer\\Code\\web.config** ให้เพิ่มรายการต่อไปนี้ในส่วน **extensionComposition**:

    ``` xml
    <add source="assembly" value="Contoso.RetailServer.SalesTransactionSignatureSample" />
    ```

7. เรียกใช้ **msbuild** สำหรับ Retail SDK ทั้งหมดเพื่อสร้างแพคเกจที่ปรับใช้ได้
8. ใช้แพคเกจผ่าน Microsoft Dynamics Lifecycle Services (LCS) หรือด้วยตนเอง สำหรับข้อมูลเพิ่มเติม โปรดดู [สร้างแพคเกจที่สามารถปรับใช้ได้](../dev-itpro/retail-sdk/retail-sdk-packaging.md)

### <a name="enable-the-digital-signature-in-offline-mode-for-modern-pos"></a>เปิดใช้งานลายเซ็นดิจิทัลในโหมดออฟไลน์ของ MODERN POS

หากต้องการเปิดใช้งานลายเซ็นดิจิทัลในโหมดออฟไลน์ของ Modern POS คุณต้องปฏิบัติตามขั้นตอนต่อไปนี้หลังจากที่คุณเรียกใช้ Modern POS บนอุปกรณ์ใหม่

1. ลงชื่อเข้าใช้ POS
2. บนหน้า **สถานะการเชื่อมต่อฐานข้อมูล** ให้ตรวจสอบให้แน่ใจว่าฐานข้อมูลออฟไลน์มีการซิงโครไนส์อย่างสมบูรณ์แล้ว เมื่อค่าของฟิลด์ **การดาวน์โหลดที่ค้างอยู่** เป็น **0 (ศูนย์)** ฐานข้อมูลจะถูกซิงโครไนส์ทั้งหมด
3. ลงชื่อออกจาก POS
4. รอสักครู่เพื่อให้ฐานข้อมูลออฟไลน์มีการซิงโครไนส์อย่างสมบูรณ์
5. ลงชื่อเข้าใช้ POS
6. บนหน้า **สถานะการเชื่อมต่อฐานข้อมูล** ให้ตรวจสอบให้แน่ใจว่าฐานข้อมูลออฟไลน์มีการซิงโครไนส์อย่างสมบูรณ์แล้ว เมื่อค่าของฟิลด์ **ธุรกรรมที่ค้างอยู่ในฐานข้อมูลออฟไลน์** เป็น **0 (ศูนย์)** ฐานข้อมูลจะถูกซิงโครไนส์ทั้งหมด
7. เริ่ม Modern POS ใหม่


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
