---
title: ปรับใช้สเกลยูนิตแบบปลายทางบนฮาร์ดแวร์แบบกำหนดเอง โดยใช้ LBD (พรีวิว)
description: หัวข้อนี้อธิบายวิธีการเตรียมใช้งานสเกลยูนิตแบบปลายทางในสถานที่ โดยใช้ฮาร์ดแวร์และการจัดวางที่กำหนดเอง ซึ่งขึ้นอยู่กับข้อมูลธุรกิจภายใน (LBD)
author: cabeln
ms.date: 04/22/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: cabeln
ms.search.validFrom: 2021-04-13
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 0ebbdaab9d6f040497d3158db2712e102b6e9aa8
ms.sourcegitcommit: 1e5a46271bf7fae2f958d2b1b666a8d2583e04a8
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/25/2021
ms.locfileid: "7678992"
---
# <a name="deploy-edge-scale-units-on-custom-hardware-using-lbd-preview"></a>ปรับใช้สเกลยูนิตแบบปลายทางบนฮาร์ดแวร์แบบกำหนดเอง โดยใช้ LBD (พรีวิว)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)] <!--KFM: Until 11/1/2021 -->

สเกลยูนิตแบบปลายทางมีบทบาทสําคัญในโทโพโลยีแบบไฮบริดแบบกระจาย สำหรับ Supply Chain Management ในโทโพโลยีแบบไฮบริด คุณสามารถกระจายปริมาณงานระหว่างฮับระบบคลาวด์ของ Supply Chain Management ของคุณ และสเกลยูนิตเพิ่มเติมใน Cloud หรือ Edge

คุณสามารถปรับใช้สเกลยูนิตแบบปลายทางได้โดยการสร้างข้อมูลธุรกิจภายใน (LBD) [สภาพแวดล้อมในสถานที่](../../fin-ops-core/dev-itpro/deployment/on-premises-deployment-landing-page.md) แล้วตั้งค่าคอนฟิกให้ฟังก์ชันเป็นสเกลยูนิตในโทโพโลยีแบบไฮบริดแบบกระจายของคุณ สำหรับ Supply Chain Management ซึ่งได้รับจากการเชื่อมโยงสภาพแวดล้อม LBD ในสถานที่กับสภาพแวดล้อม Supply Chain Management ใน Cloud ซึ่งถูกตั้งค่าคอนฟิกให้ฟังก์ชันเป็นฮับ  

ขณะนี้ สเกลยูนิตแบบปลายทางอยู่ในพรีวิว ดังนั้น คุณจึงสามารถใช้สภาพแวดล้อมชนิดนี้เฉพาะตาม [เงื่อนไขของพรีวิว](https://aka.ms/scmcnepreviewterms)เท่านั้น

หัวข้อนี้จะอธิบายวิธีตั้งค่าสภาพแวดล้อม LBD ในสถานที่เป็นสเกลยูนิตแบบปลายทาง แล้วเชื่อมโยงกับฮับ

## <a name="deployment-overview"></a>ภาพรวมของการปรับใช้

นี่คือภาพรวมของขั้นตอนการปรับใช้

1. **เปิดใช้งานช่อง LBD ในโครงการ LBD ของคุณ ใน Microsoft Dynamics Lifecycle Services (LCS)**

    ในระหว่างพรีวิว สเกลยูนิตแบบปลายทางบ LBD ตั้งเป้าหมายลูกค้า LBD ที่มีอยู่ ช่อง LBD Sandbox ที่จํากัด 60 วันเพิ่มเติม จะถูกระบุในสถานการณ์ของลูกค้าเฉพาะ

1. **ตั้งค่าและปรับใช้สภาพแวดล้อม LBD ด้วยฐานข้อมูล *ว่างเปล่า***

    ใช้ LCS เพื่อปรับใช้สภาพแวดล้อม LBD ด้วยโทโพโลยีและฐานข้อมูลว่างเปล่าล่าสุด ดูข้อมูลเพิ่มเติมที่ ส่วน [การตั้งค่าและการปรับใช้สภาพแวดล้อม LBD ด้วยฐานข้อมูลว่างเปล่า](#set-up-deploy) ในส่วนท้ายของหัวข้อนี้ คุณต้องใช้ Supply Chain Management เวอร์ชัน 10.0.19 ที่มีแพลตฟอร์มที่อัปเดต 43 หรือสูงกว่าในสภาพแวดล้อมฮับและสเกลยูนิต

1. **อัปโหลดแพคเกจเป้าหมายไปยังสินทรัพย์โครงการ LBD ใน LCS**

    จัดเตรียมแพคเกจ แอพลิเคชัน แพลตฟอร์ม และการเลือกกำหนด ที่คุณใช้ทั่วทั้งฮับและสเกลยูนิตแบบปลายทาง สำหรับข้อมูลเพิ่มเติม โปรดดูที่ส่วน [อัปโหลดแพคเกจเป้าหมายไปยังสินทรัพย์ของโครงการ LBD ใน LCS](#upload-packages) ในส่วนท้ายของหัวข้อนี้

1. **บริการสภาพแวดล้อม LBD ด้วยแพคเกจเป้าหมาย**

    ขั้นตอนนี้ช่วยให้มั่นใจว่าการสร้างและการเลือกกำหนดเดียวกันจะถูกปรับใช้บนฮับและลูกข่าย สำหรับข้อมูลเพิ่มเติม ให้ดูที่ส่วน [บริการสภาพแวดล้อม LBD ด้วยแพคเกจเป้าหมาย](#service-target-packages) ในส่วนท้ายของหัวข้อนี้

1. **ตั้งค่าคอนฟิกสเกลยูนิตและการกําหนดปริมาณงานให้เสร็จสมบูรณ์**

    สำหรับข้อมูลเพิ่มเติม ให้ดูที่ส่วน [กำหนดสเกลยูนิต LBD ของคุณให้กับฮับ](#assign-edge-to-hub) ในส่วนท้ายของหัวข้อนี้

ส่วนที่เหลือของหัวข้อนี้ให้รายละเอียดเพิ่มเติมเกี่ยวกับวิธีการดำเนินการขั้นต้องเหล่านี้ให้เสร็จสิ้น

## <a name="set-up-and-deploy-an-lbd-environment-with-an-empty-database"></a><a name="set-up-deploy"></a>ตั้งค่าและปรับใช้สภาพแวดล้อม LBD ด้วยฐานข้อมูลว่างเปล่า

ขั้นตอนนี้จะสร้างสภาพแวดล้อม LBD ที่ทำงานได้ อย่างไรก็ตาม สภาพแวดล้อมไม่ควรจะมีเวอร์ชันแอพลิเคชันและแพลตฟอร์มเดียวกันกับสภาพแวดล้อมฮับ นอกจากนี้ ยังขาดการเลือกกำหนด และยังไม่มีการเปิดใช้งานเพื่อใช้เป็นสเกลยูนิต

1. ทำตามคำแนะนำใน [ตั้งค่าและปรับใช้สภาพแวดล้อมในสถานที่ (Platform update 41 และรุ่นที่ใหม่กว่า)](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md) คุณต้องใช้ Supply Chain Management เวอร์ชัน 10.0.19 ที่มีแพลตฟอร์มที่อัปเดต 43 หรือสูงกว่าในสภาพแวดล้อมฮับและสเกลยูนิต

    > [!IMPORTANT]
    > อ่านส่วนที่เหลือของส่วนนี้ **ก่อน** คุณจะเสร็จสิ้นขั้นตอนในหัวข้อนั้น

1. ก่อนที่คุณจะอธิบายการตั้งค่าคอนฟิกของคุณในไฟล์\\ConfigTemplate.xml ของโครงสร้างพื้นฐาน ให้รันสคริปต์ต่อไปนี้:

    ```powershell
    .\Configure-ScriptsForEdgeScaleUnits.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    ```

    > [!NOTE]
    > สคริปต์นี้จะลบการตั้งค่าคอนฟิกใดๆ ที่ไม่ต้องการใช้งานสเกลยูนิตแบบปลายทาง

1. ตั้งค่าฐานข้อมูลที่มีข้อมูลว่างเปล่า ตามที่อธิบายไว้ใน [ฐานข้อมูลการตั้งค่าคอนฟิก](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md#configuredb) ใช้ไฟล์ data.csv ที่ว่างเปล่าในขั้นตอนนี้
1. ตั้งค่าสคริปต์ก่อนการปรับใช้ สำหรับข้อมูลเพิ่มเติม ดูที่ [สคริปต์ก่อนการปรับใช้และหลังการปรับใช้เอเจนต์ภายใน](../../fin-ops-core/dev-itpro/lifecycle-services/pre-post-scripts.md)

    1. คัดลอกเนื้อหาจากโฟลเดอร์ **ScaleUnit** ใน **สคริปต์โครงสร้างพื้นฐาน** ไปยังโฟลเดอร์ **สคริปต์** ในที่แบ่งใช้หน่วยจัดเก็บไฟล์ของเอเจนต์ที่ตั้งค่าในสภาพแวดล้อม พาธทั่วไปคือ \\\\lbdiscsi01\\agent\\Scripts
    2. สร้างสคริปต์ **PreDeployment.ps1** ที่จะเรียกสคริปต์โดยใช้พารามิเตอร์ที่จำเป็น ต้องวางสคริปต์การปรับใช้ล่วงหน้าในโฟลเดอร์ **สคริปต์** ในการแบ่งใช้หน่วยจัดเก็บไฟล์ของตัวแทน มิฉะนั้นจะรันไม่ได้ พาธทั่วไปคือ \\\\lbdiscsi01\\agent\\Scripts\\PreDeployment.ps1

        เนื้อหาของสคริปต์ PreDeployment.ps1 จะคล้ายกับตัวอย่างต่อไปนี้

        ```powershell
        $agentShare = '\\lbdiscsi01\agent'
        
        Write-Output "AgentShare is set to $agentShare" 
        & $agentShare\Scripts\Configure-CloudandEdge.ps1 -AgentShare $agentShare -InstanceId '@A' -DatabaseServer 'lbdsqla01.contoso.com' -DatabaseName 'AXDB'
        ```

        > [!NOTE]
        > พารามิเตอร์ InstanceId ควรเป็นสองอักขระเท่านั้น อักขระตัวแรกคือ @ และตัวที่สองสามารถเป็นอักษรตัวพิมพ์ใหญ่ใดๆ ในตัวอักษรภาษาอังกฤษ
        >
        > - ค่าที่ถูกต้อง:
        >   - @D
        >   - @X
        > - ค่าไม่ถูกต้อง:
        >   - @a
        >   - @4
        >   - @#

1. ปรับใช้สภาพแวดล้อมโดยใช้โทโพโลยีพื้นฐานล่าสุดที่พร้อมใช้งาน

## <a name="upload-target-packages-into-lbd-project-assets-in-lcs"></a><a name="upload-packages"></a>อัปโหลดแพคเกจเป้าหมายไปยังสินทรัพย์โครงการ LBD ใน LCS

ขั้นตอนนี้จัดเตรียมเวอร์ชันแอพลิเคชัน เวอร์ชันแพลตฟอร์ม และการเลือกกำหนดที่จะเปลี่ยนเป็นสภาพแวดล้อมสเกลยูนิต LBD ของคุณ

1. อัปโหลดแพคเกจแอพลิเคชัน/แพลตฟอร์มรวมเดียวกันกับที่ใช้กับสภาพแวดล้อมฮับ ไปยังไลบรารีสินทรัพย์ของโครงการ LCS ในองค์กร
1. รับสำเนาของแพคเกจที่ปรับใช้แบบกำหนดเองที่ใช้กับสภาพแวดล้อมฮับ และอัปโหลดไปยังไลบรารีสินทรัพย์ของโครงการ LCS ในองค์กร

## <a name="service-the-lbd-environment-with-target-packages"></a><a name="service-target-packages"></a>บริการสภาพแวดล้อม LBD ด้วยแพคเกจเป้าหมาย

ขั้นตอนนี้จัดเรียงเวอร์ชันแอพลิเคชัน เวอร์ชันแพลตฟอร์ม และการเลือกกำหนดในสภาพแวดล้อมสเกลยูนิต LBD ของคุณด้วยฮับ

1. บริการสภาพแวดล้อม LBD ด้วยแพคเกจแอพลิเคชัน/แพลตฟอร์มรวมที่คุณอัปโหลดในขั้นตอนก่อนหน้านี้
1. บริการสภาพแวดล้อม LBD ด้วยแพคเกจที่ปรับใช้แบบกำหนดเองที่คุณอัปโหลดในขั้นตอนก่อนหน้านี้

    ![การเลือกการรักษา >ใช้การอัปเดตใน LCS](media/cloud_edge-LBD-LCS-ServiceLBDEnv1.png "การเลือกการรักษา >ใช้การอัปเดตใน LCS")

    ![การเลือกแพคเกจการเลือกกำหนดของคุณ](media/cloud_edge-LBD-LCS-ServiceLBDEnv2.png "การเลือกแพคเกจการเลือกกำหนดของคุณ")

## <a name="assign-your-lbd-edge-scale-unit-to-a-hub"></a><a name="assign-edge-to-hub"></a>กําหนดสเกลยูนิตแบบปลายทาง LBD ของคุณให้กับฮับ

ในขณะที่สเกลยูนิตแบบปลายทางยังอยู่ในพรีวิว คุณต้องใช้ [การปรับใช้สเกลยูนิตและเครื่องมือการตั้งค่าคอนฟิก](https://github.com/microsoft/SCMScaleUnitDevTools) ที่พร้อมใช้งานบน GitHub เพื่อกําหนดสเกลยูนิตแบบปลายทาง LBD ของคุณให้กับฮับ กระบวนการช่วยให้การตั้งค่าคอนฟิก LBD สามารถทำหน้าที่เป็นสเกลยูนิตแบบปลายทางและเชื่อมโยงกับฮับ กระบวนการคล้ายกับการตั้งค่าคอนฟิกสภาพแวดล้อมการพัฒนาแบบ One-Box

1. ดาวน์โหลด [SCMScaleUnitDevTools](https://github.com/microsoft/SCMScaleUnitDevTools/releases) เวอร์ชันล่าสุด และแตกไฟล์เนื้อหา
1. สร้างสําเนาของไฟล์ `UserConfig.sample.xml` และตั้งชื่อเป็น `UserConfig.xml`
1. สร้างแอพลิเคชัน Microsoft Azure Active Directory (Azure AD) ในผู้เช่า Azure AD ของคุณ ตามที่กล่าวถึงใน [คู่มือการปรับใช้สเกลยูนิตและปริมาณงาน](https://github.com/microsoft/SCMScaleUnitDevTools/wiki/Step-by-step-usage-guide#aad-application-registrations)
    1. เมื่อสร้างแล้ว ให้นําทางไปยังฟอร์มแอพลิเคชัน Azure AD (SysAADClientTable) บนฮับของคุณ
    1. สร้างรายการใหม่และตั้งค่า **รหัสไคลเอนต์** เป็นรหัสของแอพลิเคชันที่คุณสร้างขึ้น ตั้งค่า **ชื่อ** เป็น *ScaleUnits* และ **รหัสผู้ใช้** เป็น *ผู้ดูแลระบบ*

1. สร้างแอพลิเคชัน Active Directory Federation Service (AD FS) ตามที่กล่าวถึงใน [คู่มือการปรับใช้สเกลยูนิตและปริมาณงาน](https://github.com/microsoft/SCMScaleUnitDevTools/wiki/Step-by-step-usage-guide#adfs-application-registrations)
    1. เมื่อสร้างแล้ว ให้นําทางไปยังฟอร์มแอพลิเคชัน Azure AD (SysAADClientTable) บนสเกลยูนิตแบบปลายทางของคุณ
    1. สร้างรายการใหม่และตั้งค่า **รหัสไคลเอนต์** เป็นรหัสของแอพลิเคชันที่คุณสร้างขึ้น ตั้งค่า **รหัสผู้ใช้** เป็น *ผู้ดูแลระบบ*

1. แก้ไขไฟล์ `UserConfig.xml`
    1. ภายใต้ส่วน `InterAOSAADConfiguration` ให้ป้อนข้อมูลจากแอพลิเคชัน Azure AD ที่คุณสร้างขึ้นก่อนหน้านี้
        - ในองค์ประกอบ `AppId` ให้ป้อนรหัสแอพลิเคชันของแอพลิเคชัน Azure
        - ในองค์ประกอบ `AppSecret` ให้ป้อนข้อมูลลับแอพลิเคชันของแอพลิเคชัน Azure
        - องค์ประกอบ `Authority` ต้องมี URL ที่ระบุหน่วยงานด้านความปลอดภัยของผู้เช่าของคุณ

        ```xml
        <InterAOSAADConfiguration>
            <AppId>8dab14f6-97b1-48e3-b51b-350b45f6ede5</AppId>
            <AppSecret>k6em-_7.lopty56TGUedDTVhtER-j_6anY1</AppSecret>
            <Authority>https://login.windows.net/contoso.onmicrosoft.com</Authority>
        </InterAOSAADConfiguration>
        ```

    1. ภายใต้ส่วน `ScaleUnitConfiguration` สำหรับ `ScaleUnitInstance` แรก ให้ปรับเปลี่ยนส่วน `AuthConfiguration`
        - ในองค์ประกอบ `AppId` ให้ป้อนรหัสแอพลิเคชันของแอพลิเคชัน Azure
        - ในองค์ประกอบ `AppSecret` ให้ป้อนข้อมูลลับแอพลิเคชันของแอพลิเคชัน Azure
        - องค์ประกอบ `Authority` ต้องมี URL ที่ระบุหน่วยงานด้านความปลอดภัยของผู้เช่าของคุณ

        ```xml
        <AuthConfiguration>
            <AppId>8dab14f6-97b1-48e3-b51b-350b45f6ede5</AppId>
            <AppSecret>k6em-_7.lopdz.6d3DTVOtf9Lo-j_6anY1</AppSecret>
            <Authority>https://login.windows.net/contoso.onmicrosoft.com</Authority>
        </AuthConfiguration>
        ```

    1. นอกจากนี้ สำหรับ `ScaleUnitInstance` เดียวกันนี้ ให้ตั้งค่าต่อไปนี้:
        - ในองค์ประกอบ `Domain` ให้ระบุ URL ของฮับของคุณ ตัวอย่างเช่น: `https://cloudhub.sandbox.operations.dynamics.com/`
        - ในองค์ประกอบ `EnvironmentType` โปรดตรวจสอบให้แน่ใจว่า `LCSHosted` มีการตั้งค่าแล้ว

    1. ภายใต้ส่วน `ScaleUnitConfiguration` สำหรับ `ScaleUnitInstance` ที่สอง ให้ปรับเปลี่ยนส่วน `AuthConfiguration`
        - ในองค์ประกอบ `AppId` ให้ป้อนรหัสแอพลิเคชันของแอพลิเคชัน AD FS
        - ในองค์ประกอบ `AppSecret` ให้ป้อนข้อมูลลับแอพลิเคชันของแอพลิเคชัน ADFS
        - องค์ประกอบ `Authority` ต้องมี URL ของอินสแตนซ์ AD FS ของคุณ

        ```xml
        <AuthConfiguration>
            <AppId>26b16f25-21d8-4d36-987b-62df292895aa</AppId>
            <AppSecret>iZFfObgI6lLtY9kEbBjEFV98NqI5_YZ0e5SBcWER</AppSecret>
            <Authority>https://adfs.contoso.com/adfs</Authority>
        </AuthConfiguration>
        ```

    1. นอกจากนี้ สำหรับ `ScaleUnitInstance` เดียวกันนี้ ให้ตั้งค่าต่อไปนี้:
        - ในองค์ประกอบ `Domain` ให้ระบุ URL ของสเกลยูนิตแบบปลายทางของคุณ ตัวอย่างเช่น: https://ax.contoso.com/
        - ในองค์ประกอบ `EnvironmentType` โปรดตรวจสอบให้แน่ใจว่า LBD มีการตั้งค่าแล้ว
        - ในองค์ประกอบ `ScaleUnitId` ให้ป้อนข้อมูลค่าเดียวกันกับที่คุณระบุใน `InstanceId` เมื่อตั้งค่าคอนฟิกสคริปต์การปรับใช้ล่วงหน้า `Configure-CloudandEdge.ps1`

        > [!NOTE]
        > หากคุณไม่ได้ใช้รหัสเริ่มต้น (@A) โปรดตรวจสอบให้แน่ใจว่าคุณอัปเดต ScaleUnitId ให้กับแต่ละ ConfiguredWorkload ภายใต้ส่วน Workloads

1. เปิด PowerShell และนําทางไปยังโฟลเดอร์ที่มีไฟล์ `UserConfig.xml`

1. รันเครื่องมือด้วยคำสั่งนี้

    ```powershell
    .\CLI.exe
    ```

    > [!NOTE]
    > หลังจากที่ทุกการดำเนินการจะต้องเริ่มเครื่องมืออีกครั้ง

1. ในเครื่องมือ ให้เลือก **2. จัดเตรียมสภาพแวดล้อมเกี่ยวกับการติดตั้งปริมาณงาน** จากนั้นรันขั้นตอนต่อไปนี้:
    1. เลือก **1. จัดเตรียมฮับ**
    1. เลือก **2. จัดเตรียม Scale Unit**

    > [!NOTE]
    > หากคุณไม่ได้รันคำสั่งนี้จากการติดตั้งใหม่ทั้งหมด และไม่งานล้มเหลว ให้ดำเนินการดังต่อไปนี้:
    >
    > - ลบโฟลเดอร์ทั้งหมดออกจากโฟลเดอร์ `aos-storage` (ยกเว้น `GACAssemblies`)
    > - รันคำสั่ง SQL ต่อไปนี้บนฐานข้อมูลธุรกิจของคุณ (AXDB):
    >
    > ```sql 
    > delete from storagefoler
    > ```

1. รันคำสั่ง SQL ต่อไปนี้บนฐานข้อมูลธุรกิจของคุณ (AXDB):

    ```sql
    delete from FEATUREMANAGEMENTMETADATA
    delete from FEATUREMANAGEMENTSTATE
    delete from NUMBERSEQUENCESCOPE
    ```

1. ตรวจสอบว่าได้เปิดใช้งานการติดตามการเปลี่ยนแปลงในฐานข้อมูลธุรกิจของคุณ (AXDB) แล้ว
    1. เริ่มต้น SQL Server Management Studio (SSMS)
    1. คลิกขวาที่ฐานข้อมูลธุรกิจของคุณ (AXDB) และเลือกคุณสมบัติ
    1. ในหน้าต่างที่เปิดขึ้น ให้เลือก **การติดตามการเปลี่ยนแปลง** และปรับการตั้งค่าต่อไปนี้:

        - **การติดตามการเปลี่ยนแปลง:** *จริง*
        - **รอบระยะเวลาการคงไว้:** *7*
        - **หน่วยการคงไว้:** *วัน*
        - **การล้างข้อมูลอัตโนมัติ:** *จริง*

1. ในเครื่องมือ ให้เลือก **3. ติดตั้งปริมาณงาน** จากนั้นรันขั้นตอนต่อไปนี้:
    1. เลือก **1. ติดตั้งบนฮับ**
    1. เลือก **2. ติดตั้งบน Scale Unit**

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
