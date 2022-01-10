---
title: แนวทางการปรับใช้สำหรับตัวอย่างการรวมอุปกรณ์ควบคุมสำหรับสวีเดน (ดั้งเดิม)
description: หัวข้อนี้แสดงแนวทางเกี่ยวกับการปรับใช้ตัวอย่างการรวมอุปกรณ์ควบคุมสำหรับสวีเดนจาก Retail SDK
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-3-1
ms.openlocfilehash: c0e301305fb0d99ab2f8c811f9f560bc5008e02b
ms.sourcegitcommit: 0d2de52e12fdb9928556d37a4813a67b303695dc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/21/2021
ms.locfileid: "7944901"
---
# <a name="deployment-guidelines-for-the-control-unit-integration-sample-for-sweden-legacy"></a>แนวทางการปรับใช้สำหรับตัวอย่างการรวมอุปกรณ์ควบคุมสำหรับสวีเดน (ดั้งเดิม)

[!include [banner](../includes/banner.md)]

หัวข้อนี้นําเสนอแนวทางเกี่ยวกับการปรับใช้ตัวอย่างการรวมอุปกรณ์ควบคุมสำหรับสวีเดนจากชุดการพัฒนาซอฟต์แวร์ (SDK) ของการขายปลีกบนเครื่องเสมือนของนักพัฒนา (VM) ใน Microsoft Dynamics Lifecycle Services (LCS) สำหรับข้อมูลเพิ่มเติมเกี่ยวกับตัวอย่างการรวมข้อมูลทางการเงิน ดูที่ [ตัวอย่างการรวมอุปกรณ์ควบคุมสำหรับสวีเดน](emea-swe-fi-sample.md) 

ตัวอย่างการรวมทางการเงินของสวีเดนเป็นส่วนหนึ่งของ Retail SDK สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการติดตั้ง และใช้ SDK ดูที่ [สถาปัตยกรรมของชุดการพัฒนาซอฟต์แวร์ (SDK) ของการขายปลีก](../dev-itpro/retail-sdk/retail-sdk-overview.md) ตัวอย่างนี้ประกอบด้วยส่วนขยายของ Commerce Runtime (CRT) สถานีฮาร์ดแวร์ และการขายหน้าร้าน (POS) เมื่อต้องการรันตัวอย่างนี้ คุณต้องแก้ไขและสร้าง CRT สถานีฮาร์ดแวร์ และโครงการ POS เราขอแนะนำให้คุณใช้ Retail SDK ที่ไม่ได้แก้ไขเพื่อเปลี่ยนแปลงที่อธิบายไว้ในหัวข้อนี้ เราขอแนะนำให้ใช้ระบบควบคุมต้นทาง เช่น Azure DevOps โดยที่ยังไม่มีการเปลี่ยนแปลงไฟล์ใดๆ

## <a name="development-environment"></a>สภาพแวดล้อมการพัฒนา

ปฏิบัติตามขั้นตอนต่อไปนี้เพื่อตั้งค่าสภาพแวดล้อมการพัฒนาเพื่อให้คุณสามารถทดสอบและขยายตัวอย่างได้

### <a name="enable-crt-extensions"></a>เปิดใช้งานส่วนขยาย CRT

ส่วนประกอบ CRT ส่วนขยายจะรวมอยู่ในตัวอย่าง CRT เมื่อต้องการปฏิบัติตามขั้นตอนต่อไปนี้ให้เสร็จสมบูรณ์ ให้เปิดโซลูชัน **CommerceRuntimeSamples.sln** ภายใต้ **RetailSdk\\SampleExtensions\\CommerceRuntime**

#### <a name="documentprovidercleancashsample-component"></a>ส่วนประกอบ DocumentProvider.CleanCashSample

1. ค้นหาโครงการ **Runtime.Extensions.DocumentProvider.CleanCashSample** และสร้าง
2. ในโฟลเดอร์ **Runtime.Extensions.DocumentProvider.CleanCashSample\\bin\\Debug** ให้ค้นหาไฟล์แอสเซมบลี **Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample.dll**
3. คัดลอกไฟล์แอสเซมบลีไปยังโฟลเดอร์ส่วนขยาย CRT:

    - **Commerce Scale Unit:** คัดลอกไฟล์ไปยังโฟลเดอร์ **\\bin\\ext** ภายใต้ที่ตั้งไซต์ Commerce Scale Unit ของบริการข้อมูลทางอินเทอร์เน็ต (IIS)
    - **CRT ท้องถิ่นบน POS สมัยใหม่:** คัดลอกไฟล์ไปยังโฟลเดอร์ **\\ext** ภายใต้ที่ตั้งของ Client Broker ของ CRT ท้องถิ่น

4. ค้นหาไฟล์การกำหนดค่าส่วนขยายสำหรับ CRT:

    - **Commerce Scale Unit:** ไฟล์มีชื่อว่า **commerceruntime.ext.config** และอยู่ในโฟลเดอร์ **bin\\ext** ภายใต้ที่ตั้งไซต์ Commerce Scale Unit IIS
    - **CRT เฉพาะที่บน Modern POS:** ไฟล์มีชื่อว่า **CommerceRuntime.MPOSOffline.Ext.config** และอยู่ภายใต้ที่ตั้ง Client Broker ของ CRT เฉพาะที่

5. ลงทะเบียนการเปลี่ยนแปลง CRT ในไฟล์การกำหนดค่าส่วนขยาย

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample" />
    ```

#### <a name="extension-configuration-file"></a>ไฟล์การตั้งค่าคอนฟิกส่วนขยาย

1. ค้นหาไฟล์การกำหนดค่าส่วนขยายสำหรับ CRT:

    - **Commerce Scale Unit:** ไฟล์มีชื่อว่า **commerceruntime.ext.config** และอยู่ในโฟลเดอร์ **bin\\ext** ภายใต้ที่ตั้งไซต์ Commerce Scale Unit IIS
    - **CRT เฉพาะที่บน Modern POS:** ไฟล์มีชื่อว่า **CommerceRuntime.MPOSOffline.Ext.config** และอยู่ภายใต้ที่ตั้ง Client Broker ของ CRT เฉพาะที่

2. ลงทะเบียนการเปลี่ยนแปลง CRT ในไฟล์การกำหนดค่าส่วนขยาย

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsSweden" />
    ```

### <a name="enable-hardware-station-extensions"></a>เปิดใช้งานส่วนขยายสถานีฮาร์ดแวร์

ส่วนประกอบของส่วนขยายสถานีฮาร์ดแวร์จะรวมอยู่ในตัวอย่างสถานีฮาร์ดแวร์ เมื่อต้องการปฏิบัติตามขั้นตอนต่อไปนี้ให้เสร็จสมบูรณ์ ให้เปิดโซลูชัน **HardwareStationSamples.sln** ภายใต้ **RetailSdk\\SampleExtensions\\HardwareStation**

#### <a name="cleancash-component"></a>ส่วนประกอบ CleanCash

1. ค้นหาโครงการ **HardwareStation.Extension.CleanCashSample** และสร้าง
2. ในโฟลเดอร์ **Extension.CleanCashSample\\bin\\Debug** ให้ค้นหาไฟล์แอสเซมบลี **Contoso.Commerce.HardwareStation.CleanCashSample.dll** และ **Interop.CleanCash\_1\_1.dll**
3. คัดลอกไฟล์แอสเซมบลีไปยังโฟลเดอร์ส่วนขยายของสถานีฮาร์ดแวร์:

    - **สถานีฮาร์ดแวร์ที่ใช้ร่วมกัน:** คัดลอกไฟล์ไปยังโฟลเดอร์ **bin** ที่อยู่ภายใต้ที่ตั้งของไซต์สถานีฮาร์ดแวร์ของ IIS
    - **สถานีฮาร์ดแวร์เฉพาะบน Modern POS:** คัดลอกไฟล์ไปยังที่ตั้งของ Client Broker ของ POS สมัยใหม่

4. ค้นหาไฟล์การตั้งค่าคอนฟิกสำหรับส่วนขยายสถานีฮาร์ดแวร์ มีการตั้งชื่อไฟล์เป็น **HardwareStation.Extension.config**

    - **สถานีฮาร์ดแวร์ที่ใช้ร่วมกัน:** ไฟล์อยู่ภายใต้ที่ตั้งของไซต์สถานีฮาร์ดแวร์ของ IIS
    - **สถานีฮาร์ดแวร์เฉพาะบน Modern POS:** ไฟล์อยู่ภายใต้ที่ตั้งของ Client Broker ของ POS สมัยใหม่

5. เพิ่มบรรทัดต่อไปนี้ในส่วน **องค์ประกอบ** ของไฟล์การตั้งค่าคอนฟิก

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.CleanCashSample" />
    ```

### <a name="enable-modern-pos-extension-components"></a>เปิดใช้งานส่วนประกอบส่วนขยาย POS สมัยใหม่

1. เปิดโซลูชัน **ModernPOS.sln** ภายใต้ **RetailSdk\\POS** และตรวจสอบให้แน่ใจว่าโซลูชันนั้นสามารถคอมไพล์ได้โดยไม่มีข้อผิดพลาด นอกจากนี้ ให้ตรวจสอบให้แน่ใจว่าคุณสามารถรัน POS สมัยใหม่จาก Visual Studio ได้โดยใช้คำสั่ง **Run**

    > [!NOTE]
    > POS สมัยใหม่ต้องไม่กำหนดเอง คุณต้องเปิดใช้งานการควบคุมบัญชีผู้ใช้ (UAC) และคุณต้องถอนการติดตั้งอินสแตนซ์ของ POS สมัยใหม่ที่ติดตั้งไว้ก่อนหน้านี้ตามที่ต้องการ

2. เปิดใช้งานส่วนขยายที่จะต้องโหลดในโดยการเพิ่มบรรทัดต่อไปนี้ในไฟล์ **extensions.json**

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

    > [!NOTE]
    > สำหรับข้อมูลเพิ่มเติม และตัวอย่างที่แสดงวิธีการรวมโฟลเดอร์รหัสต้นฉบับและเปิดใช้งานส่วนขยายที่จะโหลด โปรดดูคําแนะนําในไฟล์ readme.md ในโครงการ **Pos.Extensions**

3. สร้างโซลูชันใหม่
4. เรียกใช้ POS สมัยใหม่ในดีบักเกอร์ และทดสอบฟังก์ชัน

### <a name="enable-cloud-pos-extension-components"></a>เปิดใช้งานส่วนประกอบส่วนขยาย POS ระบบคลาวด์

1. เปิดโซลูชัน **CloudPOS.sln** ภายใต้ **RetailSdk\\POS** และตรวจสอบให้แน่ใจว่าโซลูชันนั้นสามารถคอมไพล์ได้โดยไม่มีข้อผิดพลาด
2. เปิดใช้งานส่วนขยายที่จะต้องโหลดในโดยการเพิ่มบรรทัดต่อไปนี้ในไฟล์ **extensions.json**

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

    > [!NOTE]
    > สำหรับข้อมูลเพิ่มเติม และตัวอย่างที่แสดงวิธีการรวมโฟลเดอร์รหัสต้นฉบับและเปิดใช้งานส่วนขยายที่จะโหลด โปรดดูคําแนะนําในไฟล์ readme.md ในโครงการ **Pos.Extensions**

3. สร้างโซลูชันใหม่
4. เรียกใช้โซลูชันโดยใช้คำสั่ง **Run** และปฏิบัติตามขั้นตอนในคู่มือ Retail SDK

## <a name="production-environment"></a>สภาพแวดล้อมการทำงานจริง

ขั้นตอนก่อนหน้าจะเปิดใช้งานส่วนขยายที่เป็นส่วนประกอบของตัวอย่างการรวมอุปกรณ์ควบคุม นอกจากนี้ คุณต้องปฏิบัติตามขั้นตอนต่อไปนี้เพื่อสร้างแพคเกจที่สามารถปรับใช้ได้ซึ่งมีส่วนประกอบของ Commerce และเพื่อใช้แพคเกจเหล่านั้นในสภาพแวดล้อมการทำงานจริง

1. ทำการเปลี่ยนแปลงต่อไปนี้ในไฟล์การตั้งค่าคอนฟิกแพคเกจภายใต้โฟลเดอร์ **RetailSdk\\Assets**:

    - ในไฟล์การกำหนดค่า **commerceruntime.ext.config** และ **CommerceRuntime.MPOSOffline.Ext.config** ให้เพิ่มรายการต่อไปนี้ลงในส่วน **องค์ประกอบ**

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample" />
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsSweden" />
        ```

    - ในไฟล์การกำหนดค่า **HardwareStation.Extension.config** ให้เพิ่มรายการต่อไปนี้ในส่วน **องค์ประกอบ**

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.CleanCashSample" />
        ```

2. การเปลี่ยนแปลงต่อไปนี้ในไฟล์การกำหนดค่าการกําหนดเองของแพคเกจ **Customization.settings** ภายใต้โฟลเดอร์ **BuildTools**:

    - เพิ่มรายการต่อไปนี้เพื่อรวมส่วนขยาย CRT ในแพคเกจที่สามารถปรับใช้ได้

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample.dll" />
        ```

    - เพิ่มรายการต่อไปนี้เพื่อรวมส่วนขยายสถานีฮาร์ดแวร์ในแพคเกจที่สามารถปรับใช้ได้

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.CleanCashSample.dll" />
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Interop.CleanCash_1_1.dll" />
        ```

3. เปิดใช้งานส่วนขยาย POS โดยเพิ่มรายการต่อไปนี้ในไฟล์ **extensions.json** ภายใต้โฟลเดอร์ **RetailSDK\\POS\\Extensions**

    ``` json
    {
        "extensionPackages": [
            {
            "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

4. เริ่ม MSBuild Command Prompt สำหรับการใช้งาน Visual Studio และเรียกใช้ **msbuild** ภายใต้โฟลเดอร์ Retail SDK เพื่อสร้างแพคเกจที่สามารถปรับใช้ได้
5. ใช้แพคเกจผ่าน LCS หรือด้วยตนเอง สำหรับข้อมูลเพิ่มเติม โปรดดู [สร้างแพคเกจที่สามารถปรับใช้ได้](../dev-itpro/retail-sdk/retail-sdk-packaging.md)
6. ทำการตั้งค่าที่ต้องใช้ให้เสร็จสิ้นตามที่อธิบายไว้ใน [การตั้งค่าการรวมกับอุปกรณ์ควบคุม](emea-swe-fi-sample.md#setting-up-the-integration-with-control-units)

## <a name="design-of-the-extensions"></a>การออกแบบของส่วนขยาย

### <a name="crt-extension-design"></a>การออกแบบของส่วนขยาย CRT

วัตถุประสงค์ของส่วนขยายที่เป็นผู้ให้บริการเอกสารทางการเงินคือการสร้างเอกสารเฉพาะบริการ และจัดการการตอบสนองจากอุปกรณ์ควบคุม

ส่วนขยาย CRT คือ **Runtime.Extensions.DocumentProvider.CleanCashSample**

สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการออกแบบของโซลูชันการรวมทางการเงิน ดูที่ [ตัวอย่างกระบวนการลงทะเบียนทางการเงินและการรวมทางการเงินสำหรับอุปกรณ์ทางการเงิน](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices)

#### <a name="request-handler"></a>ตัวจัดการคำขอ

มีตัวจัดการคำขอ **DocumentProviderCleanCash** หนึ่งตัวจัดการสำหรับตัวจัดการเอกสาร ตัวจัดการนี้ใช้ในการสร้างเอกสารทางการเงินเกี่ยวกับอุปกรณ์ควบคุม

ตัวจัดการสืบทอดมาจากอินเทอร์เฟส **INamedRequestHandler** วิธีการ **HandlerName** จะรับผิดชอบการส่งคืนชื่อของตัวจัดการ ชื่อตัวจัดการควรตรงกับชื่อผู้ให้บริการเอกสารตัวเชื่อมต่อที่ระบุในศูนย์ควบคุม Commerce

ตัวเชื่อมต่อสนับสนุนคำขอต่อไปนี้:

- **GetFiscalDocumentDocumentProviderRequest** – คำขอนี้จะมีข้อมูลเกี่ยวกับเอกสารใดที่ควรถูกสร้างขึ้น โดยจะส่งคืนเอกสารเฉพาะบริการที่ควรลงทะเบียนในอุปกรณ์ควบคุม
- **GetSupportedRegistrableEventsDocumentProviderRequest** – คำขอนี้จะส่งคืนรายการเหตุการณ์ที่จะสมัครเป็นสมาชิก ปัจจุบัน สนับสนุนเหตุการณ์การขายและเหตุการณ์การตรวจสอบ

#### <a name="configuration"></a>การกำหนดค่า

ไฟล์การตั้งค่าคอนฟิก **DocumentProviderFiscalCleanCashSample** อยู่ในโฟลเดอร์ **การตั้งค่าคอนฟิก** ของโครงการขยาย วัตถุประสงค์ของไฟล์นี้คือเพื่อเปิดใช้งานการตั้งค่าของผู้ให้บริการเอกสารที่จะตั้งค่าคอนฟิกจากศูนย์ควบคุม Commerce รูปแบบไฟล์จะสอดคล้องกับข้อกําหนดของการตั้งค่าคอนฟิกการรวมทางการเงิน มีการเพิ่มการตั้งค่ามีดังต่อไปนี้:

- การแม็ปรหัส VAT

### <a name="hardware-station-extension-design"></a>การออกแบบส่วนขยายสถานีฮาร์ดแวร์

วัตถุประสงค์ของส่วนขยายที่เป็นตัวเชื่อมต่อทางการเงินคือเพื่อสื่อสารกับอุปกรณ์ควบคุม

ส่วนขยายของสถานีฮาร์ดแวร์คือ **HardwareStation.Extension.CleanCashSample** ส่วนขยายนี้ใช้โปรโทคอล HTTP เพื่อส่งเอกสารที่ส่วนขยาย CRT สร้างขึ้นไปยังอุปกรณ์ควบคุม และยังจัดการการตอบสนองที่ได้รับจากอุปกรณ์ควบคุมด้วย

#### <a name="request-handler"></a>ตัวจัดการคำขอ

ตัวจัดการคำขอ **CleanCashHandler** เป็นจุดเข้าใช้งานเพื่อจัดการคำขอไปยังอุปกรณ์ควบคุม

ตัวจัดการสืบทอดมาจากอินเทอร์เฟส **INamedRequestHandler** วิธีการ **HandlerName** จะรับผิดชอบการส่งคืนชื่อของตัวจัดการ ชื่อตัวจัดการควรตรงกับชื่อตัวเชื่อมต่อทางการเงินที่ระบุในศูนย์ควบคุม Commerce

ตัวเชื่อมต่อสนับสนุนคำขอต่อไปนี้:

- **SubmitDocumentFiscalDeviceRequest** – คำขอนี้จะส่งเอกสารไปยังอุปกรณ์ควบคุมและส่งคืนการตอบสนองจากอุปกรณ์ควบคุม
- **IsReadyFiscalDeviceRequest** – คำขอนี้ใช้เพื่อตรวจสอบความสมบูรณ์ของอุปกรณ์ควบคุม
- **InitializeFiscalDeviceRequest** – คำขอนี้ใช้สำหรับการเริ่มต้นอุปกรณ์ควบคุม

#### <a name="configuration"></a>การกำหนดค่า

ไฟล์การตั้งค่าคอนฟิกอยู่ในโฟลเดอร์ **Configuration** ของโครงการขยาย วัตถุประสงค์ของไฟล์คือเพื่อเปิดใช้งานการตั้งค่าของตัวเชื่อมต่อทางการเงินที่จะตั้งค่าคอนฟิกจากศูนย์ควบคุม Commerce รูปแบบไฟล์จะสอดคล้องกับข้อกําหนดของการตั้งค่าคอนฟิกการรวมทางการเงิน มีการเพิ่มการตั้งค่ามีดังต่อไปนี้:

- **สตริงการเชื่อมต่อ** – การตั้งค่าการเชื่อมต่ออุปกรณ์ควบคุม
- **การหมดเวลา** – จํานวนเวลาเป็นมิลลิวินาที ซึ่งพนักงานขับรถจะรอการตอบสนองจากอุปกรณ์ควบคุม

## <a name="migrating-from-the-earlier-integration-sample"></a>การย้ายจากตัวอย่างการรวมก่อนหน้านี้

ถ้าคุณใช้ [ตัวอย่างกับการรวม POS กับอุปกรณ์ควบคุมสำหรับสวีเดน](retail-sdk-control-unit-sample.md) ก่อนหน้านี้ คุณอาจต้องย้ายจากไปยังตัวอย่างการรวมปัจจุบัน เมื่อต้องการใช้การเปลี่ยนแปลงและรับการอัปเดตคุณลักษณะต่างๆ สำหรับสวีเดนในอนาคต คุณอาจต้องอัปเกรด สร้างรหัสย่อยและปรับค่าคอนฟิกในส่วนขยายที่คุณสร้างขึ้น และสร้างโซลูชันของคุณใหม่ ไม่การเปลี่ยนแปลงหลักใดๆ จำเป็นในตรรกะส่วนขยายที่คุณสร้างขึ้น ตัวอย่างการรวมก่อนหน้านี้และการเลือกกำหนดเองของคุณจะยังคงทำงานต่อไป ถ้าไม่มีการเปลี่ยนแปลงใดๆ จากฝั่งของคุณ ดังนั้น คุณจึงสามารถวางแผน จัดเตรียม และใช้งานสำหรับสภาพแวดล้อมของคุณ

### <a name="migration-process"></a>กระบวนการย้าย

การย้ายจากตัวอย่างการรวมก่อนหน้านี้ไปยังตัวอย่างการรวมอุปกรณ์ควบคุมปัจจุบันควรเป็นไปตามแนวคิดของการอัปเดตแบบทีละขั้น กล่าวอีกอย่างคือ ควรอัปเดตส่วนประกอบของศูนย์ควบคุม Commerce และ Commerce Scale Unit ทั้งหมดก่อนที่คุณจะเริ่มอัปเดตส่วนประกอบ POS และสถานีฮาร์ดแวร์

เพื่อช่วยป้องกันสถานการณ์ที่มีการลงชื่อเหตุการณ์หรือธุรกรรมสองครั้ง (กล่าวคือ มีการลงชื่อโดยทั้งส่วนขยายก่อนหน้านี้และส่วนขยายปัจจุบัน) หรือโดยที่ไม่สามารถลงชื่อเหตุการณ์หรือธุรกรรมได้เนื่องจากการตั้งค่าคอนฟิกขาดหายไป ขอแนะนำว่าคุณควรปิดอุปกรณ์ POS และสถานีฮาร์ดแวร์ทั้งหมดที่ใช้ตัวอย่างก่อนหน้านี้ แล้วอัปเดตพร้อมกัน การอัปเดตพร้อมกันนี้สามารถเกิดขึ้นได้ ตัวอย่างเช่น ตามแต่ละร้านค้า โดยการอัปเดตโพรไฟล์ฟังก์ชันของร้านค้าและโปรไฟล์ฮาร์ดแวร์ของสถานีฮาร์ดแวร์

กระบวนการย้ายควรประกอบด้วยขั้นตอนต่อไปนี้

1. อัปเดตส่วนประกอบของศูนย์ควบคุม Commerce
1. อัปเดตส่วนประกอบ Commerce Scale Unit และเปิดใช้งานส่วนขยายของตัวอย่างปัจจุบัน
1. ตรวจสอบให้แน่ใจว่าธุรกรรมออฟไลน์ทั้งหมดถูกซิงค์จากอุปกรณ์ MPOS ที่เปิดใช้งานแบบออฟไลน์
1. ปิดอุปกรณ์ทั้งหมดที่ใช้ส่วนประกอบของตัวอย่างก่อนหน้านี้
1. ทำการตั้งค่าที่ต้องใช้ให้เสร็จสิ้นตามที่อธิบายไว้ใน [การตั้งค่าการรวมกับอุปกรณ์ควบคุม](emea-swe-fi-sample.md#setting-up-the-integration-with-control-units)
1. อัปเดตส่วนประกอบของสถานี POS และสถานีฮาร์ดแวร์ ปิดใช้งานส่วนขยายที่เป็นส่วนประกอบของตัวอย่างก่อนหน้านี้ และเปิดใช้งานส่วนขยายของตัวอย่างปัจจุบัน

    > [!NOTE]
    > นี้ขึ้นอยู่กับชนิดของสภาพแวดล้อม คุณสามารถค้นหารายละเอียดทางเทคนิคเพิ่มเติมเกี่ยวกับกระบวนการย้ายในส่วน [การย้ายในสภาพแวดล้อมการพัฒนา](#migration-in-a-development-environment) หรือ [การย้ายในส่วนสภาพแวดล้อมการผลิต](#migration-in-a-production-environment) ของหัวข้อนี้

### <a name="migration-in-a-development-environment"></a>การย้ายในสภาพแวดล้อมการพัฒนา

#### <a name="update-crt"></a>อัพเดต CRT

1. ค้นหาโครงการ **Runtime.Extensions.DocumentProvider.CleanCashSample** และสร้าง
2. ในโฟลเดอร์ **Runtime.Extensions.DocumentProvider.CleanCashSample\\bin\\Debug** ให้ค้นหาไฟล์แอสเซมบลี **Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample.dll**
3. คัดลอกไฟล์แอสเซมบลีไปยังโฟลเดอร์ส่วนขยาย CRT:

    - **Commerce Scale Unit:** คัดลอกไฟล์ไปยังโฟลเดอร์ **\\bin\\ext** ภายใต้ที่ตั้งไซต์ Commerce Scale Unit ของ IIS
    - **CRT ท้องถิ่นบน POS สมัยใหม่:** คัดลอกไฟล์ไปยังโฟลเดอร์ **\\ext** ภายใต้ที่ตั้งของ Client Broker ของ CRT ท้องถิ่น

4. ค้นหาไฟล์การกำหนดค่าส่วนขยายสำหรับ CRT:

    - **Commerce Scale Unit:** ไฟล์มีชื่อว่า **CommerceRuntime.ext.config** และอยู่ในโฟลเดอร์ **bin\\ext** ภายใต้ที่ตั้งไซต์ Commerce Scale Unit IIS
    - **CRT เฉพาะที่บน Modern POS:** ไฟล์มีชื่อว่า **CommerceRuntime.MPOSOffline.Ext.config** และอยู่ในโฟลเดอร์ **bin\\ext** ภายใต้ที่ตั้ง Client Broker ของ CRT เฉพาะที่

    > [!WARNING]
    > ห้าม **ไม่ให้** แก้ไขไฟล์ CommerceRuntime.config และ CommerceRuntime.MPOSOffline.config ไฟล์เหล่านี้ไม่ได้มีไว้เพื่อการกำหนดเองใดๆ

5. ค้นหาและลบส่วนขยาย CRT ก่อนหน้านี้ออกจากไฟล์การตั้งค่าคอนฟิกส่วนขยาย

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.FiscalRegisterReceiptSample" />
    ```

    > [!WARNING]
    > อย่าผ่านขั้นตอนนี้จนกว่าคุณจะอัปเดตอุปกรณ์ POS ทั้งหมดที่ใช้งานกับอินสแตนซ์ CRT นี้

6. ลงทะเบียนส่วนขยาย CRT ตัวอย่างปัจจุบันในไฟล์การตั้งค่าคอนฟิกส่วนขยายโดยเพิ่มบรรทัดต่อไปนี้

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample" />
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsSweden" />
    ```

#### <a name="update-hardware-station"></a>อัปเดตสถานีฮาร์ดแวร์

1. ค้นหาโครงการ **HardwareStation.Extension.CleanCashSample** และสร้าง
2. ในโฟลเดอร์ **Extension.CleanCashSample\\bin\\Debug** ให้ค้นหาไฟล์แอสเซมบลี **Contoso.Commerce.HardwareStation.CleanCashSample.dll** และ **Interop.CleanCash\_1\_1.dll**
3. คัดลอกไฟล์แอสเซมบลีไปยังโฟลเดอร์ส่วนขยายของสถานีฮาร์ดแวร์:

    - **สถานีฮาร์ดแวร์ที่ใช้ร่วมกัน:** คัดลอกไฟล์ไปยังโฟลเดอร์ **bin** ที่อยู่ภายใต้ที่ตั้งของไซต์สถานีฮาร์ดแวร์ของ IIS
    - **สถานีฮาร์ดแวร์เฉพาะบน Modern POS:** คัดลอกไฟล์ไปยังที่ตั้งของ Client Broker ของ POS สมัยใหม่

4. ค้นหาไฟล์การตั้งค่าคอนฟิกส่วนขยาย **HardwareStation.Extension.config**:

    - **สถานีฮาร์ดแวร์ระยะไกล:** ไฟล์อยู่ภายใต้ที่ตั้งของไซต์สถานีฮาร์ดแวร์ของ IIS
    - **สถานีฮาร์ดแวร์เฉพาะที่บน Modern POS:** ไฟล์อยู่ภายใต้ที่ตั้งของ Client Broker ของ POS สมัยใหม่

    > [!WARNING]
    > ห้าม **ไม่ให้** แก้ไขไฟล์ CommerceRuntime.config และ CommerceRuntime.MPOSOffline.config ไฟล์เหล่านี้ไม่ได้มีไว้เพื่อการกำหนดเองใดๆ

5. ค้นหาและลบส่วนขยายสถานีฮาร์ดแวร์ก่อนหน้านี้ออกจากไฟล์การตั้งค่าคอนฟิกส่วนขยาย

    # <a name="retail-73-and-earlier"></a>[Retail 7.3 และก่อนหน้านี้](#tab/retail-7-3)

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
    ```

    # <a name="retail-731-and-later"></a>[Retail 7.3.1 และรุ่นที่ใหม่กว่า](#tab/retail-7-3-1)

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
    ```

    # <a name="retail-100-and-later"></a>[Retail 10.0 และรุ่นที่ใหม่กว่า](#tab/retail-10-0)

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.FiscalRegisterSample" />
    ```
    ---

6. เพิ่มบรรทัดต่อไปนี้ในส่วน **องค์ประกอบ** ของไฟล์การตั้งค่าคอนฟิกส่วนขยาย

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.CleanCashSample" />
    ```

#### <a name="update-modern-pos"></a>อัปเดต Modern POS

1. เปิดโซลูชัน **CloudPOS.sln** ภายใต้ **RetailSdk\\POS**
2. ปิดใช้งานส่วนขยาย POS ก่อนหน้านี้โดยการเอารายการต่อไปนี้ออกจากไฟล์ **extensions.json**

    ``` json
    {
        "baseUrl": "FiscalRegisterSample"
    }
    ```

2. เปิดใช้งานส่วนขยาย POS ตัวอย่างปัจจุบันในโดยการเพิ่มบรรทัดต่อไปนี้ในไฟล์ **extensions.json**

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

#### <a name="update-cloud-pos"></a>อัปเดต Cloud POS

1. เปิดโซลูชัน **ModernPOS.sln** ภายใต้ **RetailSdk\\POS**
2. ปิดใช้งานส่วนขยาย POS ก่อนหน้านี้โดยการเอารายการต่อไปนี้ออกจากไฟล์ **extensions.json**

    ``` json
    {
        "baseUrl": "FiscalRegisterSample"
    }
    ```

2. เปิดใช้งานส่วนขยาย POS ตัวอย่างปัจจุบันในโดยการเพิ่มบรรทัดต่อไปนี้ในไฟล์ **extensions.json**

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

### <a name="migration-in-a-production-environment"></a>การย้ายในสภาพแวดล้อมการทำงานจริง

#### <a name="update-crt"></a>อัพเดต CRT

1. ลบส่วนขยาย CRT ก่อนหน้านี้ออกจากไฟล์การตั้งค่าคอนฟิก **CommerceRuntime.ext.config** และ **CommerceRuntime.MPOSOffline.Ext.config** ภายใต้โฟลเดอร์ **RetailSdk\\Assets**

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.FiscalRegisterReceiptSample" />
    ```

    > [!WARNING]
    > อย่าผ่านขั้นตอนนี้จนกว่าคุณจะอัปเดตอุปกรณ์ POS ทั้งหมดที่ใช้งานกับอินสแตนซ์ CRT นี้

2. เปิดใชง้านส่วนขยาย CRT ตัวอย่างปัจจุบันโดยการทำการเปลี่ยนแปลงต่อไปนี้ในไฟล์การตั้งค่าคอนฟิก **CommerceRuntime.ext.config** และ **CommerceRuntime.MPOSOffline.Ext.config** ภายใต้โฟลเดอร์ **RetailSdk\\Assets**

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample" />
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsSweden" />
    ```

3. ในไฟล์การกําหนดเองของแพคเกจ **Customization.settings** ภายใต้โฟลเดอร์ **BuildTools** ให้เพิ่มรายการต่อไปนี้เพื่อรวมส่วนขยาย CRT ตัวอย่างปัจจุบันในแพคเกจที่ปรับใช้ได้

    ``` xml
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample.dll" />
    ```

#### <a name="update-hardware-station"></a>อัปเดตสถานีฮาร์ดแวร์

1. ลบส่วนขยายสถานีฮาร์ดแวร์ก่อนหน้านี้ออกโดยการแก้ไขไฟล์การตั้งค่าคอนฟิก **HardwareStation.Extension.config**

    # <a name="retail-73-and-earlier"></a>[Retail 7.3 และก่อนหน้านี้](#tab/retail-7-3)

    ลบส่วนต่อไปนี้ออกจากไฟล์การตั้งค่าคอนฟิก **HardwareStation.Shared.config** และ **HardwareStation.Dedicated.config**

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
    ```

    # <a name="retail-731-and-later"></a>[Retail 7.3.1 และรุ่นที่ใหม่กว่า](#tab/retail-7-3-1)

    ลบส่วนต่อไปนี้ออกจากไฟล์การตั้งค่าคอนฟิก **HardwareStation.Extension.config**

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
    ```

    # <a name="retail-100-and-later"></a>[Retail 10.0 และรุ่นที่ใหม่กว่า](#tab/retail-10-0)

    ลบส่วนต่อไปนี้ออกจากไฟล์การตั้งค่าคอนฟิก **HardwareStation.Extension.config**

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.FiscalRegisterSample" />
    ```
    ---

2. เปิดใช้งานส่วนขยายสถานีฮาร์ดแวร์ตัวอย่างปัจจุบันโดยเพิ่มรายการต่อไปนี้ลงในส่วน **องค์ประกอบ** ในไฟล์การตั้งค่าคอนฟิก **HardwareStation.Extension.config**

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.CleanCashSample" />
    ```

3. การเปลี่ยนแปลงต่อไปนี้ในไฟล์การกำหนดค่าการกําหนดเองของแพคเกจ **Customization.settings** ภายใต้โฟลเดอร์ **BuildTools**:

    - ลบรายการต่อไปนี้ออกเพื่อไม่รวมส่วนขยายสถานีฮาร์ดแวร์ก่อนหน้าจากแพคเกจที่สามารถปรับใช้ได้

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample.dll" />
        ```

    - เพิ่มรายการต่อไปนี้เพื่อรวมส่วนขยายสถานีฮาร์ดแวร์ตัวอย่างปัจจุบันในแพคเกจที่สามารถปรับใช้ได้

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.CleanCashSample.dll" />
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Interop.CleanCash_1_1.dll" />
        ```

#### <a name="update-modern-pos"></a>อัปเดต Modern POS

1. เปิดโซลูชัน **CloudPOS.sln** ที่ **RetailSdk\\POS**
2. ปิดใช้งานส่วนขยาย POS ก่อนหน้านี้:

    - ในไฟล์ **tsconfig.json** ให้เพิ่มโฟลเดอร์ **FiscalRegisterSample** ลงในรายการไม่รวม
    - เอารายการต่อไปนี้ออกจากไฟล์ **extensions.json** ภายใต้โฟลเดอร์ **RetailSDK\\POS\\Extensions**

        ``` json
        {
            "baseUrl": "FiscalRegisterSample"
        }
        ```

3. เปิดใช้งานส่วนขยาย POS ตัวอย่างปัจจุบันโดยเพิ่มรายการต่อไปนี้ในไฟล์ **extensions.json** ภายใต้โฟลเดอร์ **RetailSDK\\POS\\Extensions**

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

#### <a name="update-cloud-pos"></a>อัปเดต Cloud POS

1. เปิดโซลูชัน **ModernPOS.sln** ภายใต้ **RetailSdk\\POS**
2. ปิดใช้งานส่วนขยาย POS ก่อนหน้านี้:

    - ในไฟล์ **tsconfig.json** ให้เพิ่มโฟลเดอร์ **FiscalRegisterSample** ลงในรายการไม่รวม
    - เอารายการต่อไปนี้ออกจากไฟล์ **extensions.json** ภายใต้โฟลเดอร์ **RetailSDK\\POS\\Extensions**

        ``` json
        {
            "baseUrl": "FiscalRegisterSample"
        }
        ```

3. เปิดใช้งานส่วนขยาย POS ตัวอย่างปัจจุบันโดยเพิ่มรายการต่อไปนี้ในไฟล์ **extensions.json** ภายใต้โฟลเดอร์ **RetailSDK\\POS\\Extensions**

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

#### <a name="create-deployable-packages"></a>สร้างแพคเกจที่สามารถปรับใช้ได้

เรียกใช้ **msbuild** สำหรับ Retail SDK ทั้งหมดเพื่อสร้างแพคเกจที่ปรับใช้ได้ ใช้แพคเกจผ่าน LCS หรือด้วยตนเอง สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [การบรรจุสินค้าของ Retail SDK](../dev-itpro/retail-sdk/retail-sdk-packaging.md)
