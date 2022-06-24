---
title: แนวทางการปรับใช้งานตัวอย่างการรวมเครื่องพิมพ์ทางการเงินของโปแลนด์ (ดั้งเดิม)
description: บทความนี้แสดงแนวทางเกี่ยวกับการปรับใช้ตัวอย่างการรวมเครื่องพิมพ์ทางการเงินสำหรับโปแลนด์จากชุดการพัฒนาซอฟต์แวร์ (SDK) ของการขายปลีกของ Microsoft Dynamics 365 Commerce
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-3-1
ms.openlocfilehash: 3de7559838a8d8caf64993a468f06ba2d50fff46
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8851168"
---
# <a name="deployment-guidelines-for-the-fiscal-printer-integration-sample-for-poland-legacy"></a>แนวทางการปรับใช้งานตัวอย่างการรวมเครื่องพิมพ์ทางการเงินของโปแลนด์ (ดั้งเดิม)

[!include[banner](../includes/banner.md)]

บทความนี้นําเสนอแนวทางเกี่ยวกับการปรับใช้ตัวอย่างการรวมเครื่องพิมพ์ทางการเงินสำหรับโปแลนด์จากชุดการพัฒนาซอฟต์แวร์ (SDK) ของการขายปลีกของ Microsoft Dynamics 365 Commerce บนเครื่องเสมือนของนักพัฒนา (VM) ใน Microsoft Dynamics Lifecycle Services (LCS) สำหรับข้อมูลเพิ่มเติมเกี่ยวกับตัวอย่างการรวมข้อมูลทางการเงิน ดูที่ [ตัวอย่างการรวมเครื่องพิมพ์ทางการเงินสำหรับโปแลนด์](emea-pol-fpi-sample.md) 

ตัวอย่างการรวมทางการเงินของโปแลนด์เป็นส่วนหนึ่งของ Retail SDK สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการติดตั้ง และใช้ SDK ดูที่ [สถาปัตยกรรมของชุดการพัฒนาซอฟต์แวร์ (SDK) ของการขายปลีก](../dev-itpro/retail-sdk/retail-sdk-overview.md) ตัวอย่างนี้ประกอบด้วยส่วนขยายของ Commerce Runtime (CRT) และสถานีฮาร์ดแวร์ เมื่อต้องการเรียกใช้ตัวอย่างนี้ คุณต้องแก้ไขและสร้าง CRT และโครงการสถานีฮาร์ดแวร์ เราขอแนะนำให้คุณใช้ Retail SDK ที่ไม่ได้แก้ไขเพื่อเปลี่ยนแปลงที่อธิบายไว้ในบทความนี้ เราขอแนะนำให้ใช้ระบบควบคุมต้นทาง เช่น Azure DevOps โดยที่ยังไม่มีการเปลี่ยนแปลงไฟล์ใดๆ

## <a name="development-environment"></a>สภาพแวดล้อมการพัฒนา

ปฏิบัติตามขั้นตอนต่อไปนี้เพื่อตั้งค่าสภาพแวดล้อมการพัฒนาเพื่อให้คุณสามารถทดสอบและขยายตัวอย่างได้

### <a name="commerce-runtime-extension-components"></a>ส่วนประกอบส่วนขยาย Commerce Runtime

ส่วนประกอบส่วนขยาย CRT จะรวมอยู่ใน Retail SDK เมื่อต้องการปฏิบัติตามขั้นตอนต่อไปนี้ให้เสร็จสมบูรณ์ ให้เปิดโซลูชัน **CommerceRuntimeSamples.sln** ภายใต้ **RetailSdk\\SampleExtensions\\CommerceRuntime**

1. ค้นหาโครงการ **Runtime.Extensions.DocumentProvider.PosnetSample** และสร้าง
2. ในโฟลเดอร์ **Extensions.DocumentProvider.PosnetSample\\bin\\Debug** ให้ค้นหาไฟล์แอสเซมบลี **Contoso.Commerce.Runtime.Extensions.DocumentProvider.PosnetSample.dll**
3. คัดลอกไฟล์แอสเซมบลีไปยังโฟลเดอร์ส่วนขยาย CRT:

    - **Commerce Scale Unit:** คัดลอกไฟล์ไปยังโฟลเดอร์ **\\bin\\ext** ภายใต้ที่ตั้งไซต์ Commerce Scale Unit ของบริการข้อมูลทางอินเทอร์เน็ต (IIS)
    - **CRT ท้องถิ่นบน POS สมัยใหม่:** คัดลอกไฟล์ไปยังโฟลเดอร์ **\\ext** ภายใต้ที่ตั้งของ Client Broker ของ CRT ท้องถิ่น

4. ค้นหาไฟล์การกำหนดค่าส่วนขยายสำหรับ CRT:

    - **Commerce Scale Unit:** ไฟล์มีชื่อว่า **commerceruntime.ext.config** และอยู่ในโฟลเดอร์ **bin\\ext** ภายใต้ที่ตั้งไซต์ Commerce Scale Unit IIS
    - **CRT เฉพาะที่บน Modern POS:** ไฟล์มีชื่อว่า **CommerceRuntime.MPOSOffline.Ext.config** และอยู่ภายใต้ที่ตั้ง Client Broker ของ CRT เฉพาะที่

5. ลงทะเบียนการเปลี่ยนแปลง CRT ในไฟล์การกำหนดค่าส่วนขยาย

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.Extensions.DocumentProvider.PosnetSample" />
    ```

6. เริ่ม Commerce Service ใหม่:

    - **Commerce Scale Unit:** เริ่มไซต์ Commerce service ใหม่จากโปรแกรมจัดการ IIS
    - **Client broker:** สิ้นสุดกระบวนการ **dllhost.exe** ใน Task Manager แล้วเริ่ม MODERN POS ใหม่

### <a name="hardware-station-extension-components"></a>ส่วนประกอบส่วนขยายสถานีฮาร์ดแวร์

ส่วนประกอบส่วนขยายสถานีฮาร์ดแวร์จะรวมอยู่ใน Retail SDK เมื่อต้องการปฏิบัติตามขั้นตอนต่อไปนี้ให้เสร็จสมบูรณ์ ให้เปิดโซลูชัน **HardwareStationSamples.sln** ภายใต้ **RetailSdk\\SampleExtensions\\HardwareStation**

1. ค้นหาโครงการ **HardwareStation.Extension.PosnetThermalFVFiscalPrinterSample** และสร้าง
2. ในโฟลเดอร์ **Extension.Posnet.ThermalFVFiscalPrinterSample\\bin\\Debug** ให้ค้นหาไฟล์แอสเซมบลี **Contoso.Commerce.HardwareStation.PosnetThermalFVFiscalPrinterSample.dll**
3. คัดลอกไฟล์แอสเซมบลีไปยังเครื่องสถานีฮาร์ดแวร์ที่ปรับใช้:

    - **สถานีฮาร์ดแวร์ระยะไกล:** คัดลอกไฟล์ไปยังโฟลเดอร์ **bin** ที่อยู่ภายใต้ที่ตั้งของไซต์สถานีฮาร์ดแวร์ของ IIS คัดลอกไลบรารีโปรแกรมควบคุมเครื่องพิมพ์ (**libposcmbth.dll**, **libcmbth\_serial.dll** และ **cmbth\_pl.lng**)

4. ค้นหาไฟล์การตั้งค่าคอนฟิกสำหรับส่วนขยายสถานีฮาร์ดแวร์ มีการตั้งชื่อไฟล์เป็น **HardwareStation.Extension.config**:

    - **สถานีฮาร์ดแวร์ระยะไกล:** ไฟล์อยู่ภายใต้ที่ตั้งของไซต์สถานีฮาร์ดแวร์ของ IIS

5. เพิ่มบรรทัดต่อไปนี้ในส่วน **องค์ประกอบ** ของไฟล์การตั้งค่าคอนฟิก

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.PosnetThermalFVFiscalPrinterSample" />
    ```

6. เริ่มบริการสถานีฮาร์ดแวร์ใหม่:

    - **สถานีฮาร์ดแวร์ระยะไกล:** เริ่มไซต์สถานีฮาร์ดแวร์จาก IIS Manager ใหม่

## <a name="production-environment"></a>สภาพแวดล้อมการทำงานจริง

ในขั้นตอนก่อนหน้า คุณจะเปิดใช้งานส่วนขยายที่เป็นส่วนประกอบของตัวอย่างการรวมบริการลงทะเบียนทางการเงิน นอกจากนี้ คุณต้องปฏิบัติตามขั้นตอนต่อไปนี้เพื่อสร้างแพคเกจที่สามารถปรับใช้ได้ซึ่งมีส่วนประกอบของ Commerce และเพื่อใช้แพคเกจเหล่านั้นในสภาพแวดล้อมการทำงานจริง

1. ทำการเปลี่ยนแปลงต่อไปนี้ในไฟล์การตั้งค่าคอนฟิกแพคเกจภายใต้โฟลเดอร์ **RetailSdk\\Assets**:

    - ในไฟล์การกำหนดค่า **commerceruntime.ext.config** และ **CommerceRuntime.MPOSOffline.Ext.config** ให้เพิ่มรายการต่อไปนี้ลงในส่วน **องค์ประกอบ**

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.Extensions.DocumentProvider.PosnetSample" />
        ```

    - ในไฟล์การกำหนดค่า **HardwareStation.Extension.config** ให้เพิ่มรายการต่อไปนี้ในส่วน **องค์ประกอบ**

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.PosnetThermalFVFiscalPrinterSample" />
        ```

1. การเปลี่ยนแปลงต่อไปนี้ในไฟล์การกำหนดค่าการกําหนดเองของแพคเกจ **Customization.settings** ภายใต้โฟลเดอร์ **BuildTools**:

    - เพิ่มรายการต่อไปนี้เพื่อรวมส่วนขยาย CRT ในแพคเกจที่สามารถปรับใช้ได้

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.Extensions.DocumentProvider.PosnetSample.dll"/>
        ```

    - เพิ่มรายการต่อไปนี้เพื่อรวมส่วนขยายสถานีฮาร์ดแวร์ในแพคเกจที่สามารถปรับใช้ได้

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.PosnetThermalFVFiscalPrinterSample.dll"/>
        ```

1. เริ่ม MSBuild Command Prompt สำหรับการใช้งาน Visual Studio และเรียกใช้ **msbuild** ภายใต้โฟลเดอร์ Retail SDK เพื่อสร้างแพคเกจที่สามารถปรับใช้ได้
1. ใช้แพคเกจผ่าน LCS หรือด้วยตนเอง สำหรับข้อมูลเพิ่มเติม โปรดดู [สร้างแพคเกจที่สามารถปรับใช้ได้](../dev-itpro/retail-sdk/retail-sdk-packaging.md)

## <a name="design-of-extensions"></a>การออกแบบของส่วนขยาย

ตัวอย่างการรวมเครื่องพิมพ์ทางการเงินของโปแลนด์ยึดตาม [ฟังก์ชันการรวมทางการเงิน](fiscal-integration-for-retail-channel.md) สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการออกแบบของโซลูชันการรวมทางการเงิน ดูที่ [ภาพรวมของตัวอย่างการออกแบบการรวมทางการเงิน](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services)

### <a name="commerce-runtime-extension-design"></a>การออกแบบส่วนขยาย Commerce Runtime

วัตถุประสงค์ของส่วนขยายที่เป็นผู้ให้บริการเอกสารทางการเงินคือการสร้างเอกสารเฉพาะเครื่องพิมพ์ และจัดการการตอบสนองจากเครื่องพิมพ์ทางการเงิน

ส่วนขยาย CRT คือ **Runtime.Extensions.DocumentProvider.PosnetSample** ส่วนขยายนี้จะสร้างชุดของคำสั่งเฉพาะเครื่องพิมพ์ในรูปแบบ JavaScript Object Notation (JSON) ที่กําหนดโดยข้อกําหนด POSNET 19-3678

สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการออกแบบของโซลูชันการรวมทางการเงิน ดูที่ [ตัวอย่างกระบวนการลงทะเบียนทางการเงินและการรวมทางการเงินสำหรับอุปกรณ์และบริการทางการเงิน](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services)

#### <a name="request-handler"></a>ตัวจัดการคำขอ

ตัวจัดการคำขอ **DocumentProviderPosnetProtocol** เป็นจุดป้อนข้อมูลของคำขอในการสร้างเอกสารจากเครื่องพิมพ์ทางการเงิน

ตัวจัดการสืบทอดมาจากอินเทอร์เฟส **INamedRequestHandler** วิธีการ **HandlerName** จะรับผิดชอบการส่งคืนชื่อของตัวจัดการ ชื่อตัวจัดการควรตรงกับชื่อผู้ให้บริการเอกสารตัวเชื่อมต่อที่ระบุในศูนย์ควบคุม Commerce

ตัวเชื่อมต่อสนับสนุนคำขอต่อไปนี้:

- **GetFiscalDocumentDocumentProviderRequest** – คำขอนี้จะมีข้อมูลเกี่ยวกับเอกสารใดที่ควรถูกสร้างขึ้น โดยจะส่งคืนเอกสารเฉพาะเครื่องพิมพ์ที่ควรลงทะเบียนในเครื่องพิมพ์ทางการเงิน
- **GetSupportedRegistrableEventsDocumentProviderRequest** – คำขอนี้จะส่งคืนรายการเหตุการณ์ที่จะสมัครเป็นสมาชิก ปัจจุบัน เหตุการณ์ต่อไปนี้ได้รับการสนับสนุน: การขาย การพิมพ์รายงาน X และการพิมพ์รายงาน Z

#### <a name="configuration"></a>การกำหนดค่า

ไฟล์การตั้งค่าคอนฟิกอยู่ในโฟลเดอร์ **Configuration** ของโครงการขยาย วัตถุประสงค์ของไฟล์นี้คือเพื่อเปิดใช้งานการตั้งค่าของผู้ให้บริการเอกสารที่จะตั้งค่าคอนฟิกจากศูนย์ควบคุม Commerce รูปแบบไฟล์จะสอดคล้องกับข้อกําหนดของการตั้งค่าคอนฟิกการรวมทางการเงิน มีการเพิ่มการตั้งค่ามีดังต่อไปนี้:

- การแมปอัตรา VAT
- การแมปชนิดการชำระเงิน
- ชนิดของการชำระเงินผ่านเงินฝากธนาคาร

### <a name="hardware-station-extension-design"></a>การออกแบบส่วนขยายสถานีฮาร์ดแวร์

วัตถุประสงค์ของส่วนขยายที่เป็นตัวเชื่อมต่อทางการเงินคือเพื่อสื่อสารกับเครื่องพิมพ์ทางการเงิน

ส่วนขยายของสถานีฮาร์ดแวร์คือ **HardwareStation.Extension.PosnetThermalFVFiscalPrinterSample** ส่วนขยายนี้จะเรียกฟังก์ชันของไดรเวอร์ POSNET เพื่อส่งคำสั่งที่ส่วนขยาย CRT สร้างขึ้นไปยังเครื่องพิมพ์ทางการเงิน และยังจัดการข้อผิดพลาดของอุปกรณ์ด้วย

#### <a name="request-handler"></a>ตัวจัดการคำขอ

ตัวจัดการคำขอ **FiscalPrinterHandler** คือจุดเข้าใช้งานที่จะจัดการคำขอไปยังอุปกรณ์ต่อพ่วงทางการเงิน

ตัวจัดการสืบทอดมาจากอินเทอร์เฟส **INamedRequestHandler** วิธีการ **HandlerName** จะรับผิดชอบการส่งคืนชื่อของตัวจัดการ ชื่อตัวจัดการควรตรงกับชื่อตัวเชื่อมต่อทางการเงินที่ระบุในศูนย์ควบคุม Commerce

ตัวเชื่อมต่อสนับสนุนคำขอต่อไปนี้:

- **SubmitDocumentFiscalDeviceRequest** – คำขอนี้จะส่งเอกสารไปยังเครื่องพิมพ์และส่งคืนการตอบสนองจากเครื่องพิมพ์ทางการเงิน
- **IsReadyFiscalDeviceRequest** – คำขอนี้ใช้เพื่อตรวจสอบความสมบูรณ์ของอุปกรณ์
- **InitializeFiscalDeviceRequest** – คำขอนี้ใช้สำหรับการเริ่มต้นเครื่องพิมพ์

#### <a name="configuration"></a>การกำหนดค่า

ไฟล์การตั้งค่าคอนฟิกอยู่ในโฟลเดอร์ **Configuration** ของโครงการขยาย วัตถุประสงค์ของไฟล์คือเพื่อเปิดใช้งานการตั้งค่าของตัวเชื่อมต่อที่จะตั้งค่าคอนฟิกจากศูนย์ควบคุม Commerce รูปแบบไฟล์จะสอดคล้องกับข้อกําหนดของการตั้งค่าคอนฟิกการรวมทางการเงิน มีการเพิ่มการตั้งค่ามีดังต่อไปนี้:

- **สตริงการเชื่อมต่อ** – สตริงที่อธิบายรายละเอียดของการเชื่อมต่อกับอุปกรณ์ในรูปแบบที่พนักงานขับรถสนับสนุน สำหรับข้อมูลเพิ่มเติม ให้ดูที่คู่มือไดรเวอร์ POSNET
- **วันที่และเวลาของการซิงโครไนส์** – ค่าที่ระบุว่าวันที่และเวลาของเครื่องพิมพ์ต้องถูกซิงค์กับสถานีฮาร์ดแวร์ที่เชื่อมต่อหรือไม่
- **การหมดเวลาของอุปกรณ์** – จํานวนเวลาเป็นมิลลิวินาที ซึ่งพนักงานขับรถจะรอการตอบสนองจากอุปกรณ์ สำหรับข้อมูลเพิ่มเติม ให้ดูที่คู่มือไดรเวอร์ POSNET
