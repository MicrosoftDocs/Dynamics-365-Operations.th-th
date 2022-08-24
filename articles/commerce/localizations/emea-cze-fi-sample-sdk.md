---
title: แนวทางการปรับใช้งานตัวอย่างการรวมบริการลงทะเบียนทางการเงินของสาธารณรัฐเช็ก (ดั้งเดิม)
description: บทความนี้แสดงแนวทางเกี่ยวกับการปรับใช้ตัวอย่างการรวมทางการเงินสำหรับสาธารณรัฐเช็กจากชุดการพัฒนาซอฟต์แวร์ (SDK) ของการขายปลีกของ Microsoft Dynamics 365 Commerce
author: EvgenyPopovMBS
ms.date: 03/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-03-01
ms.openlocfilehash: d689e5b48fb8274a58d0c3a18e70b598aca2c310
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9287550"
---
# <a name="deployment-guidelines-for-the-fiscal-registration-service-integration-sample-for-the-czech-republic-legacy"></a>แนวทางการปรับใช้งานตัวอย่างการรวมบริการลงทะเบียนทางการเงินของสาธารณรัฐเช็ก (ดั้งเดิม)

[!include [banner](../includes/banner.md)]

บทความนี้นําเสนอแนวทางเกี่ยวกับการปรับใช้ตัวอย่างการรวมบริการลงทะเบียนทางการเงินสำหรับสาธารณรัฐเช็กจากชุดการพัฒนาซอฟต์แวร์ (SDK) ของการขายปลีกของ Microsoft Dynamics 365 Commerce บนเครื่องเสมือนของนักพัฒนา (VM) ใน Microsoft Dynamics Lifecycle Services (LCS) สำหรับข้อมูลเพิ่มเติมเกี่ยวกับตัวอย่างการรวมข้อมูลทางการเงิน ดูที่ [ตัวอย่างการรวมบริการลงทะเบียนทางการเงินสำหรับสาธารณรัฐเช็ก](emea-cze-fi-sample.md) 

ตัวอย่างการรวมทางการเงินของสาธารณรัฐเช็กเป็นส่วนหนึ่งของ Retail SDK สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการติดตั้ง และใช้ SDK ดูที่ [สถาปัตยกรรมของชุดการพัฒนาซอฟต์แวร์ (SDK) ของการขายปลีก](../dev-itpro/retail-sdk/retail-sdk-overview.md) ตัวอย่างนี้ประกอบด้วยส่วนขยายของ Commerce Runtime (CRT) และสถานีฮาร์ดแวร์ เมื่อต้องการเรียกใช้ตัวอย่างนี้ คุณต้องแก้ไขและสร้าง CRT และโครงการสถานีฮาร์ดแวร์ เราขอแนะนำให้คุณใช้ Retail SDK ที่ไม่ได้แก้ไขเพื่อเปลี่ยนแปลงที่อธิบายไว้ในบทความนี้ เราขอแนะนำให้ใช้ระบบควบคุมต้นทาง เช่น Azure DevOps โดยที่ยังไม่มีการเปลี่ยนแปลงไฟล์ใดๆ

## <a name="development-environment"></a>สภาพแวดล้อมการพัฒนา

ปฏิบัติตามขั้นตอนต่อไปนี้เพื่อตั้งค่าสภาพแวดล้อมการพัฒนาเพื่อให้คุณสามารถทดสอบและขยายตัวอย่างได้

### <a name="enable-commerce-runtime-extensions"></a>เปิดใช้งานส่วนขยาย Commerce Runtime

ส่วนประกอบ CRT ส่วนขยายจะรวมอยู่ในตัวอย่าง CRT เมื่อต้องการปฏิบัติตามขั้นตอนต่อไปนี้ให้เสร็จสมบูรณ์ ให้เปิดโซลูชัน **CommerceRuntimeSamples.sln** ภายใต้ **RetailSdk\\SampleExtensions\\CommerceRuntime**

#### <a name="documentproviderefrsample-component"></a>ส่วนประกอบ DocumentProvider.EFRSample

1. ค้นหาโครงการ **Runtime.Extensions.DocumentProvider.EFRSample** และสร้าง
2. ในโฟลเดอร์ **Runtime.Extensions.DocumentProvider.EFRSample\\bin\\Debug** ให้ค้นหาไฟล์แอสเซมบลี **Contoso.Commerce.Runtime.DocumentProvider.EFRSample.dll**
3. คัดลอกไฟล์แอสเซมบลีไปยังโฟลเดอร์ส่วนขยาย CRT:

    - **Commerce Scale Unit:** คัดลอกไฟล์ไปยังโฟลเดอร์ **\\bin\\ext** ภายใต้ที่ตั้งไซต์ Commerce Scale Unit ของบริการข้อมูลทางอินเทอร์เน็ต (IIS)
    - **CRT ท้องถิ่นบน POS สมัยใหม่:** คัดลอกไฟล์ไปยังโฟลเดอร์ **\\ext** ภายใต้ที่ตั้งของ Client Broker ของ CRT ท้องถิ่น

4. ค้นหาไฟล์การกำหนดค่าส่วนขยายสำหรับ CRT:

    - **Commerce Scale Unit:** ไฟล์มีชื่อว่า **commerceruntime.ext.config** และอยู่ในโฟลเดอร์ **bin\\ext** ภายใต้ที่ตั้งไซต์ Commerce Scale Unit IIS
    - **CRT เฉพาะที่บน Modern POS:** ไฟล์มีชื่อว่า **CommerceRuntime.MPOSOffline.Ext.config** และอยู่ภายใต้ที่ตั้ง Client Broker ของ CRT เฉพาะที่

5. ลงทะเบียนการเปลี่ยนแปลง CRT ในไฟล์การกำหนดค่าส่วนขยาย

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EFRSample" />
    ```

#### <a name="documentproviderdatamodelefr-component"></a>ส่วนประกอบ DocumentProvider.DataModelEFR

1. ค้นหาโครงการ **Runtime.Extensions.DocumentProvider.DataModelEFR** และสร้าง
2. ในโฟลเดอร์ **Runtime.Extensions.DocumentProvider.DataModelEFR\\bin\\Debug** ให้ค้นหาไฟล์แอสเซมบลี **Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll**
3. คัดลอกไฟล์แอสเซมบลีไปยังโฟลเดอร์ส่วนขยาย CRT:

    - **Commerce Scale Unit:** คัดลอกไฟล์ไปยังโฟลเดอร์ **\\bin\\ext** ภายใต้ที่ตั้งไซต์ Commerce Scale Unit ของ IIS
    - **CRT ท้องถิ่นบน POS สมัยใหม่:** คัดลอกไฟล์ไปยังโฟลเดอร์ **\\ext** ภายใต้ที่ตั้งของ Client Broker ของ CRT ท้องถิ่น

4. ค้นหาไฟล์การกำหนดค่าส่วนขยายสำหรับ CRT:

    - **Commerce Scale Unit:** ไฟล์มีชื่อว่า **commerceruntime.ext.config** และอยู่ในโฟลเดอร์ **bin\\ext** ภายใต้ที่ตั้งไซต์ Commerce Scale Unit IIS
    - **CRT เฉพาะที่บน Modern POS:** ไฟล์มีชื่อว่า **CommerceRuntime.MPOSOffline.Ext.config** และอยู่ภายใต้ที่ตั้ง Client Broker ของ CRT เฉพาะที่

5. ลงทะเบียนการเปลี่ยนแปลง CRT ในไฟล์การกำหนดค่าส่วนขยาย

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
    ```

#### <a name="extension-configuration-file"></a>ไฟล์การตั้งค่าคอนฟิกส่วนขยาย

1. ค้นหาไฟล์การกำหนดค่าส่วนขยายสำหรับ CRT:

    - **Commerce Scale Unit:** ไฟล์มีชื่อว่า **commerceruntime.ext.config** และอยู่ในโฟลเดอร์ **bin\\ext** ภายใต้ที่ตั้งไซต์ Commerce Scale Unit IIS
    - **CRT เฉพาะที่บน Modern POS:** ไฟล์มีชื่อว่า **CommerceRuntime.MPOSOffline.Ext.config** และอยู่ภายใต้ที่ตั้ง Client Broker ของ CRT เฉพาะที่

2. ลงทะเบียนการเปลี่ยนแปลง CRT ในไฟล์การกำหนดค่าส่วนขยาย

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsCzechia" />
    ```

### <a name="enable-fiscal-connector-extensions"></a>เปิดใช้งานส่วนขยายของตัวเชื่อมต่อทางการเงิน

คุณสามารถเปิดใช้งานส่วนขยายของตัวเชื่อมต่อทางการเงินบน [สถานีฮาร์ดแวร์](fiscal-integration-for-retail-channel.md#fiscal-registration-is-done-via-a-device-connected-to-the-hardware-station) หรือ [เครื่องบันทึกเงินสด POS](fiscal-integration-for-retail-channel.md#fiscal-registration-is-done-via-a-device-or-service-in-the-local-network)

### <a name="enable-hardware-station-extensions"></a>เปิดใช้งานส่วนขยายสถานีฮาร์ดแวร์

ส่วนประกอบของส่วนขยายสถานีฮาร์ดแวร์จะรวมอยู่ในตัวอย่างสถานีฮาร์ดแวร์ เมื่อต้องการปฏิบัติตามขั้นตอนต่อไปนี้ให้เสร็จสมบูรณ์ ให้เปิดโซลูชัน **HardwareStationSamples.sln** ภายใต้ **RetailSdk\\SampleExtensions\\HardwareStation**

#### <a name="efrsample-component"></a>ส่วนประกอบ EFRSample

1. ค้นหาโครงการ **HardwareStation.Extension.EFRSample** และสร้าง
2. ในโฟลเดอร์ **Extension.EFRSample\\bin\\Debug** ค้นหาไฟล์แอสเซมบลีต่อไปนี้:

    - Contoso.Commerce.HardwareStation.EFRSample.dll
    - Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll

3. คัดลอกไฟล์แอสเซมบลีไปยังโฟลเดอร์ส่วนขยายของสถานีฮาร์ดแวร์:

    - **สถานีฮาร์ดแวร์ที่ใช้ร่วมกัน:** คัดลอกไฟล์ไปยังโฟลเดอร์ **bin** ที่อยู่ภายใต้ที่ตั้งของไซต์สถานีฮาร์ดแวร์ของ IIS
    - **สถานีฮาร์ดแวร์เฉพาะบน Modern POS:** คัดลอกไฟล์ไปยังที่ตั้งของ Client Broker ของ POS สมัยใหม่

4. ค้นหาไฟล์การตั้งค่าคอนฟิกสำหรับส่วนขยายสถานีฮาร์ดแวร์ มีการตั้งชื่อไฟล์เป็น **HardwareStation.Extension.config**

    - **สถานีฮาร์ดแวร์ที่ใช้ร่วมกัน:** ไฟล์อยู่ภายใต้ที่ตั้งของไซต์สถานีฮาร์ดแวร์ของ IIS
    - **สถานีฮาร์ดแวร์เฉพาะบน Modern POS:** ไฟล์อยู่ภายใต้ที่ตั้งของ Client Broker ของ POS สมัยใหม่

5. เพิ่มบรรทัดต่อไปนี้ในส่วน **องค์ประกอบ** ของไฟล์การตั้งค่าคอนฟิก

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.EFRSample.dll" />
    ```

#### <a name="enable-pos-extensions"></a>เปิดใช้งานส่วนขยาย POS

ตัวอย่างส่วนขยาย POS อยู่ในโฟลเดอร์ **src\\FiscalIntegration\\PosFiscalConnectorSample** ของที่เก็บ [โซลูชัน Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/)

เมื่อต้องการใช้ตัวอย่างส่วนขยาย POS ใน SDK ดั้งเดิม ให้ทำตามขั้นตอนเหล่านี้

1. คัดลอกโฟลเดอร์ **Pos.Extension** ไปยังโฟลเดอร์ **ส่วนขยาย** POS ของ SDK ดั้งเดิม (ตัวอย่าง `C:\RetailSDK\src\POS\Extensions`)
1. เปลี่ยนชื่อสําเนาของโฟลเดอร์ **Pos.Extension** เป็น **PosFiscalConnector**
1. ลบโฟลเดอร์และไฟล์ต่อไปนี้ออกจากโฟลเดอร์ **PosFiscalConnector**:

    - bin / ช่องเก็บ
    - DataService
    - devDependencies
    - ไลบรารี
    - obj
    - Contoso.PosFiscalConnectorSample.Pos.csproj
    - RetailServerEdmxModel.g.xml
    - tsconfig.json

1. เปิดโซลูชัน **CloudPos.sln** หรือ **ModernPos.sln**
1. ในโครงการ **Pos.Extensions** มีโฟลเดอร์ **PosFiscalConnector**
1. เปิดไฟล์ **extensions.json** แล้วเพิ่มส่วนขยาย **PosFiscalConnector**
1. สร้าง SDK

### <a name="production-environment"></a>สภาพแวดล้อมการทำงานจริง

ขั้นตอนก่อนหน้าจะเปิดใช้งานส่วนขยายที่เป็นส่วนประกอบของตัวอย่างการรวมบริการลงทะเบียนทางการเงิน นอกจากนี้ คุณต้องปฏิบัติตามขั้นตอนต่อไปนี้เพื่อสร้างแพคเกจที่สามารถปรับใช้ได้ซึ่งมีส่วนประกอบของ Commerce และเพื่อใช้แพคเกจเหล่านั้นในสภาพแวดล้อมการทำงานจริง

1. ทำการเปลี่ยนแปลงต่อไปนี้ในไฟล์การตั้งค่าคอนฟิกแพคเกจภายใต้โฟลเดอร์ **RetailSdk\\Assets**

    - ในไฟล์การกำหนดค่า **commerceruntime.ext.config** และ **CommerceRuntime.MPOSOffline.Ext.config** ให้เพิ่มรายการต่อไปนี้ลงในส่วน **องค์ประกอบ**

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EFRSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsCzechia" />
        ```

    - ในไฟล์การกำหนดค่า **HardwareStation.Extension.config** ให้เพิ่มรายการต่อไปนี้ในส่วน **องค์ประกอบ**

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.EFRSample" />
        ```

2. การเปลี่ยนแปลงต่อไปนี้ในไฟล์การกำหนดค่าการกําหนดเองของแพคเกจ **Customization.settings** ภายใต้โฟลเดอร์ **BuildTools**

    - เพิ่มรายการต่อไปนี้เพื่อรวมส่วนขยาย CRT ในแพคเกจที่สามารถปรับใช้ได้

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.EFRSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll" />
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll" />
        ```

    - เพิ่มรายการต่อไปนี้เพื่อรวมส่วนขยายสถานีฮาร์ดแวร์ในแพคเกจที่สามารถปรับใช้ได้

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.EFRSample" />
        ```

3. เริ่ม MSBuild Command Prompt สำหรับการใช้งาน Visual Studio และเรียกใช้ **msbuild** ภายใต้โฟลเดอร์ Retail SDK เพื่อสร้างแพคเกจที่สามารถปรับใช้ได้
4. ใช้แพคเกจผ่าน LCS หรือด้วยตนเอง สำหรับข้อมูลเพิ่มเติม โปรดดู [สร้างแพคเกจที่สามารถปรับใช้ได้](../dev-itpro/retail-sdk/retail-sdk-packaging.md)
5. ทำการตั้งค่าที่ต้องใช้ซึ่งอธิบายไว้ใน [ตั้งค่า Commerce สำหรับสาธารณรัฐเช็ก](emea-cze-fi-sample.md#set-up-commerce-for-the-czech-republic)

## <a name="design-of-extensions"></a>การออกแบบของส่วนขยาย

ตัวอย่างการรวมบริการลงทะเบียนทางการเงินของสาธารณรัฐเช็กยึดตาม [ฟังก์ชันการรวมทางการเงิน](fiscal-integration-for-retail-channel.md) สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการออกแบบของโซลูชันการรวมทางการเงิน ดูที่ [ภาพรวมของตัวอย่างการออกแบบการรวมทางการเงิน](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services)

### <a name="commerce-runtime-extension-design"></a>การออกแบบส่วนขยาย Commerce Runtime

วัตถุประสงค์ของส่วนขยายที่เป็นผู้ให้บริการเอกสารทางการเงินคือการสร้างเอกสารเฉพาะบริการ และจัดการการตอบสนองจากบริการลงทะเบียนทางการเงิน

ส่วนขยาย CRT คือ **Runtime.Extensions.DocumentProvider.EFRSample**

#### <a name="request-handler"></a>ตัวจัดการคำขอ

มีตัวจัดการคำขอ **DocumentProviderEFRFiscalCZE** หนึ่งตัวจัดการสำหรับตัวจัดการเอกสาร ตัวจัดการนี้ใช้ในการสร้างเอกสารทางการเงินเกี่ยวกับบริการลงทะเบียนทางการเงิน

ตัวจัดการสืบทอดมาจากอินเทอร์เฟส **INamedRequestHandler** วิธีการ **HandlerName** จะรับผิดชอบการส่งคืนชื่อของตัวจัดการ ชื่อตัวจัดการควรตรงกับชื่อผู้ให้บริการเอกสารตัวเชื่อมต่อที่ระบุใน Commerce headquarters

ตัวเชื่อมต่อสนับสนุนคำขอต่อไปนี้:

- **GetFiscalDocumentDocumentProviderRequest** – คำขอนี้จะมีข้อมูลเกี่ยวกับเอกสารใดที่ควรถูกสร้างขึ้น โดยจะส่งคืนเอกสารเฉพาะบริการที่ควรลงทะเบียนในบริการลงทะเบียนทางการเงิน
- **GetSupportedRegistrableEventsDocumentProviderRequest** – คำขอนี้จะส่งคืนรายการเหตุการณ์ที่จะสมัครเป็นสมาชิก ปัจจุบัน เหตุการณ์ต่อไปนี้ได้รับการสนับสนุน: การขาย การฝากเงินเข้าบัญชีลูกค้า และการฝากเงินตามใบสั่งของลูกค้า
- **GetFiscalRegisterResponseToSaveDocumentProviderRequest** – คำขอนี้จะส่งคืนการตอบสนองจากบริการการลงทะเบียนทางการเงิน การตอบสนองนี้จะเป็นอนุกรมเพื่อให้เป็นสตริงเพื่อความพร้อมในการบันทึก

#### <a name="configuration"></a>การกำหนดค่า

ไฟล์การตั้งค่าคอนฟิก **DocumentProviderFiscalEFRSampleCzech** อยู่ในโฟลเดอร์ **Configuration** ของโครงการขยาย วัตถุประสงค์ของไฟล์นี้คือเพื่อเปิดใช้งานการตั้งค่าของผู้ให้บริการเอกสารที่จะตั้งค่าคอนฟิกจาก Commerce headquarters รูปแบบไฟล์จะสอดคล้องกับข้อกําหนดของการตั้งค่าคอนฟิกการรวมทางการเงิน มีการเพิ่มการตั้งค่ามีดังต่อไปนี้:

- การแมปอัตรา VAT
- กลุ่ม VAT เริ่มต้น
- กลุ่ม VAT การฝากเงิน

### <a name="hardware-station-extension-design"></a>การออกแบบส่วนขยายสถานีฮาร์ดแวร์

วัตถุประสงค์ของส่วนขยายที่เป็นตัวเชื่อมต่อทางการเงินคือเพื่อสื่อสารกับบริการลงทะเบียนทางการเงิน

ส่วนขยายของสถานีฮาร์ดแวร์ชื่อ **HardwareStation.Extension.EFRSample** ส่วนขยายนี้ใช้โปรโทคอล HTTP หรือ HTTPS เพื่อส่งเอกสารที่ส่วนขยาย CRT สร้างขึ้นไปยังบริการลงทะเบียนทางการเงิน และยังจัดการการตอบสนองที่ได้รับจากบริการลงทะเบียนทางการเงินด้วย

#### <a name="request-handler"></a>ตัวจัดการคำขอ

ตัวจัดการคำขอ **EFRHandler** เป็นจุดเข้าใช้งานเพื่อจัดการคำขอไปยังบริการลงทะเบียนทางการเงิน

ตัวจัดการสืบทอดมาจากอินเทอร์เฟส **INamedRequestHandler** วิธีการ **HandlerName** จะรับผิดชอบการส่งคืนชื่อของตัวจัดการ ชื่อตัวจัดการควรตรงกับชื่อตัวเชื่อมต่อทางการเงินที่ระบุใน Commerce headquarters

ตัวเชื่อมต่อสนับสนุนคำขอต่อไปนี้:

- **SubmitDocumentFiscalDeviceRequest** – คำขอนี้จะส่งเอกสารไปยังบริการลงทะเบียนทางการเงินและส่งคืนการตอบสนองจากบริการลงทะเบียนทางการเงิน
- **IsReadyFiscalDeviceRequest** – คำขอนี้ใช้เพื่อตรวจสอบความสมบูรณ์ของบริการลงทะเบียนทางการเงิน
- **InitializeFiscalDeviceRequest** – คำขอนี้ใช้สำหรับการเริ่มต้นบริการลงทะเบียนทางการเงิน

#### <a name="configuration"></a>การกำหนดค่า

ไฟล์การตั้งค่าคอนฟิกอยู่ในโฟลเดอร์ **Configuration** ของโครงการขยาย วัตถุประสงค์ของไฟล์คือเพื่อเปิดใช้งานการตั้งค่าของตัวเชื่อมต่อทางการเงินที่จะตั้งค่าคอนฟิกจาก Commerce headquarters รูปแบบไฟล์จะสอดคล้องกับข้อกําหนดของการตั้งค่าคอนฟิกการรวมทางการเงิน มีการเพิ่มการตั้งค่ามีดังต่อไปนี้:

- **ที่อยู่ปลายทาง** – URL ของบริการลงทะเบียนทางการเงิน
- **การหมดเวลา** – จํานวนเวลาเป็นมิลลิวินาที ซึ่งตัวเชื่อมต่อจะรอการตอบสนองจากบริการลงทะเบียนทางการเงิน

### <a name="pos-fiscal-connector-extension-design"></a>การออกแบบส่วนขยายของตัวเชื่อมต่อทางการเงิน POS

วัตถุประสงค์ของส่วนขยายตัวเชื่อมต่อทางการเงิน POS คือเพื่อสื่อสารกับบริการลงทะเบียนทางการเงินจาก POS โดยจะใช้โพรโทคอล HTTPS สำหรับการสื่อสาร

#### <a name="fiscal-connector-factory"></a>แฟคทอรีตัวเชื่อมต่อทางการเงิน

แฟกทอรีตัวเชื่อมต่อทางการเงินจะแมปชื่อตัวเชื่อมต่อกับการใช้งานตัวเชื่อมต่อทางการเงิน และอยู่ในไฟล์ **Pos.Extension\\Connectors\\FiscalConnectorFactory.ts** ชื่อตัวเชื่อมต่อควรตรงกับชื่อตัวเชื่อมต่อทางการเงินที่ระบุใน Commerce headquarters

#### <a name="efr-fiscal-connector"></a>ตัวเชื่อมต่อทางการเงิน EFR

ตัวเชื่อมต่อทางการเงิน EFR อยู่ในไฟล์ **Pos.Extension\\Connectors\\Efr\\EfrFiscalConnector.ts** โดยจะใช้อินเทอร์เฟส **IFiscalConnector** ที่รองรับคำขอต่อไปนี้

- **FiscalRegisterSubmitDocumentClientRequest** – คำขอนี้จะส่งเอกสารไปยังบริการลงทะเบียนทางการเงินและส่งคืนการตอบสนองจากบริการลงทะเบียนทางการเงิน
- **FiscalRegisterIsReadyClientRequest** – คำขอนี้ใช้เพื่อตรวจสอบความสมบูรณ์ของบริการลงทะเบียนทางการเงิน
- **FiscalRegisterInitializeClientRequest** – คำขอนี้ใช้สำหรับการเริ่มต้นบริการลงทะเบียนทางการเงิน

#### <a name="configuration"></a>โครงแบบ

ไฟล์การตั้งค่าคอนฟิกอยู่ในโฟลเดอร์ **src\\FiscalIntegration\\Efr\\Configurations\\Connectors** ของที่เก็บ [โซลูชัน Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) วัตถุประสงค์ของไฟล์คือเพื่อเปิดใช้งานการตั้งค่าของตัวเชื่อมต่อทางการเงินที่จะตั้งค่าคอนฟิกจาก Commerce headquarters รูปแบบไฟล์จะสอดคล้องกับข้อกําหนดของการตั้งค่าคอนฟิกการรวมทางการเงิน มีการเพิ่มการตั้งค่ามีดังต่อไปนี้:

- **ที่อยู่ปลายทาง** – URL ของบริการลงทะเบียนทางการเงิน
- **การหมดเวลา** – จํานวนเวลาเป็นมิลลิวินาที ซึ่งตัวเชื่อมต่อจะรอการตอบสนองจากบริการลงทะเบียนทางการเงิน
