---
title: ปรับใช้สเกลยูนิตแบบปลายทางบนฮาร์ดแวร์แบบกำหนดเอง โดยใช้ LBD
description: หัวข้อนี้อธิบายวิธีการเตรียมใช้งานสเกลยูนิตแบบปลายทางในสถานที่ โดยใช้ฮาร์ดแวร์และการจัดวางที่กำหนดเอง ซึ่งขึ้นอยู่กับข้อมูลธุรกิจภายใน (LBD)
author: cabeln
ms.date: 11/29/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: cabeln
ms.search.validFrom: 2021-04-13
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 8913debd614827ef66ded88e0da61663ca9c6b3d
ms.sourcegitcommit: 29d34f2fd509e2bb27d8572cd57c397d014a8e38
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/07/2021
ms.locfileid: "7894729"
---
# <a name="deploy-edge-scale-units-on-custom-hardware-using-lbd"></a>ปรับใช้สเกลยูนิตแบบปลายทางบนฮาร์ดแวร์แบบกำหนดเอง โดยใช้ LBD

[!include [banner](../includes/banner.md)]

สเกลยูนิตแบบปลายทางมีบทบาทสําคัญในโทโพโลยีแบบไฮบริดแบบกระจาย สำหรับ Supply Chain Management ในโทโพโลยีแบบไฮบริด คุณสามารถกระจายปริมาณงานระหว่างฮับระบบคลาวด์ของ Supply Chain Management ของคุณ และสเกลยูนิตเพิ่มเติมใน Cloud หรือ Edge

คุณสามารถปรับใช้สเกลยูนิตแบบปลายทางได้โดยการสร้างข้อมูลธุรกิจภายใน (LBD) [สภาพแวดล้อมในสถานที่](../../fin-ops-core/dev-itpro/deployment/on-premises-deployment-landing-page.md) แล้วตั้งค่าคอนฟิกให้ฟังก์ชันเป็นสเกลยูนิตในโทโพโลยีแบบไฮบริดแบบกระจายของคุณ สำหรับ Supply Chain Management ซึ่งได้รับจากการเชื่อมโยงสภาพแวดล้อม LBD ในสถานที่กับสภาพแวดล้อม Supply Chain Management ใน Cloud ซึ่งถูกตั้งค่าคอนฟิกให้ฟังก์ชันเป็นฮับ  

หัวข้อนี้จะอธิบายวิธีตั้งค่าสภาพแวดล้อม LBD ในสถานที่เป็นสเกลยูนิตแบบปลายทาง แล้วเชื่อมโยงกับฮับ

## <a name="deployment-overview"></a>ภาพรวมของการปรับใช้

นี่คือภาพรวมของขั้นตอนการปรับใช้

1. **เปิดใช้งานช่อง LBD ในโครงการ LBD ของคุณ ใน Microsoft Dynamics Lifecycle Services (LCS)**

1. **ตั้งค่าและปรับใช้สภาพแวดล้อม LBD ด้วยฐานข้อมูล *ว่างเปล่า***

    ใช้ LCS เพื่อปรับใช้สภาพแวดล้อม LBD ด้วยโทโพโลยีและฐานข้อมูลว่างเปล่าล่าสุด ดูข้อมูลเพิ่มเติมที่ ส่วน [การตั้งค่าและการปรับใช้สภาพแวดล้อม LBD ด้วยฐานข้อมูลว่างเปล่า](#set-up-deploy) ในส่วนท้ายของหัวข้อนี้ คุณต้องใช้ Supply Chain Management รุ่น 10.0.21 หรือรุ่นใหม่กว่า ผ่านฮับและสเกลยูนิต

1. **อัปโหลดแพคเกจเป้าหมายไปยังสินทรัพย์โครงการ LBD ใน LCS**

    จัดเตรียมแพคเกจ แอปพลิเคชัน แพลตฟอร์ม และการเลือกกำหนด ที่คุณใช้ทั่วทั้งฮับและสเกลยูนิตแบบปลายทาง สำหรับข้อมูลเพิ่มเติม โปรดดูที่ส่วน [อัปโหลดแพคเกจเป้าหมายไปยังสินทรัพย์ของโครงการ LBD ใน LCS](#upload-packages) ในส่วนท้ายของหัวข้อนี้

1. **บริการสภาพแวดล้อม LBD ด้วยแพคเกจเป้าหมาย**

    ขั้นตอนนี้ช่วยให้มั่นใจว่าการสร้างและการเลือกกำหนดเดียวกันจะถูกปรับใช้บนฮับและลูกข่าย สำหรับข้อมูลเพิ่มเติม ให้ดูที่ส่วน [บริการสภาพแวดล้อม LBD ด้วยแพคเกจเป้าหมาย](#service-target-packages) ในส่วนท้ายของหัวข้อนี้

1. **ตั้งค่าคอนฟิกสเกลยูนิตและการกําหนดปริมาณงานให้เสร็จสมบูรณ์**

    สำหรับข้อมูลเพิ่มเติม ให้ดูที่ส่วน [กำหนดสเกลยูนิต LBD ของคุณให้กับฮับ](#assign-edge-to-hub) ในส่วนท้ายของหัวข้อนี้

ส่วนที่เหลือของหัวข้อนี้ให้รายละเอียดเพิ่มเติมเกี่ยวกับวิธีการดำเนินการขั้นต้องเหล่านี้ให้เสร็จสิ้น

## <a name="set-up-and-deploy-an-lbd-environment-with-an-empty-database"></a><a name="set-up-deploy"></a>ตั้งค่าและปรับใช้สภาพแวดล้อม LBD ด้วยฐานข้อมูลว่างเปล่า

ขั้นตอนนี้จะสร้างสภาพแวดล้อม LBD ที่ทำงานได้ อย่างไรก็ตาม สภาพแวดล้อมไม่ควรจะมีเวอร์ชันแอปพลิเคชันและแพลตฟอร์มเดียวกันกับสภาพแวดล้อมฮับ นอกจากนี้ ยังขาดการเลือกกำหนด และยังไม่มีการเปิดใช้งานเพื่อใช้เป็นสเกลยูนิต

1. ทำตามคำแนะนำใน [ตั้งค่าและปรับใช้สภาพแวดล้อมในสถานที่ (Platform update 41 และรุ่นที่ใหม่กว่า)](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md) คุณต้องใช้ Supply Chain Management รุ่น 10.0.21 หรือรุ่นใหม่กว่า ผ่านฮับและสเกลยูนิต นอกจากนี้ คุณต้องใช้เวอร์ชัน 2.12.0 หรือรุ่นใหม่กว่าของสคริปต์โครงสร้างพื้นฐาน 

    > [!IMPORTANT]
    > อ่านส่วนที่เหลือของส่วนนี้ **ก่อน** คุณจะเสร็จสิ้นขั้นตอนในหัวข้อนั้น

1. ก่อนที่คุณจะอธิบายการตั้งค่าคอนฟิกของคุณในไฟล์\\ConfigTemplate.xml ของโครงสร้างพื้นฐาน ให้รันสคริปต์ต่อไปนี้:

    ```powershell
    .\Configure-ScriptsForEdgeScaleUnits.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    ```

    > [!NOTE]
    > สคริปต์นี้จะลบการตั้งค่าคอนฟิกใดๆ ที่ไม่ต้องการใช้งานสเกลยูนิตแบบปลายทาง

1. ตั้งค่าฐานข้อมูลที่มีข้อมูลว่างเปล่า ตามที่อธิบายไว้ใน [ฐานข้อมูลการตั้งค่าคอนฟิก](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md#configuredb) ใช้ไฟล์ data.csv ที่ว่างเปล่าในขั้นตอนนี้
1. หลังจากที่คุณดำเนินการขั้นตอน [การตั้งค่าคอนฟิกฐานข้อมูล](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md#configuredb) เสร็จสิ้นแล้ว ให้รันสคริปต์ต่อไปนี้เพื่อตั้งค่าคอนฟิกฐานข้อมูล Scale Unit Alm Orchestrator

    > [!NOTE]
    > อย่าตั้งค่าคอนฟิกฐานข้อมูล Financial Reporting ระหว่างขั้นตอน [การตั้งค่าคอนฟิกฐานข้อมูล](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md#configuredb)

    ```powershell
    .\Initialize-Database.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -ComponentName EdgeScaleUnit
    ```

    สคริปต์ Initializte-Database.ps1 จะดำเนินการดังต่อไปนี้:

    1. สร้างฐานข้อมูลเปล่าที่โดยให้ชื่อว่า **ScaleUnitAlmDb**
    2. แม็ปผู้ใช้กับบทบาทฐานข้อมูล อ้างอิงจากตารางต่อไปนี้

        | ผู้ใช้            | ชนิด | บทบาทฐานข้อมูล |
        |-----------------|------|---------------|
        | svc-LocalAgent$ | gMSA | db\_เจ้าของ     |

1. ทำตามคำแนะนำอย่างต่อเนื่องใน [ตั้งค่าและปรับใช้สภาพแวดล้อมในสถานที่ (Platform update 41 และรุ่นที่ใหม่กว่า)](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md)
1. หลังจากที่คุณดำเนินการขั้นตอน [ตั้งค่าคอนฟิก AD FS](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md#configuredb) เสร็จสิ้นแล้ว ให้ปฏิบัติตามขั้นตอนต่อไปนี้

    1. สร้างแอปพลิเคชัน Active Directory Federation Services (AD FS) ใหม่ที่จะเปิดใช้งานบริการ Alm Orchestration เพื่อสื่อสารกับ Application Object Server (AOS) ของคุณ

        ```powershell
        # Host URL is your DNS record\host name for accessing the AOS
        .\Create-ADFSServerApplicationForEdgeScaleUnits.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -HostUrl 'https://ax.d365ffo.onprem.contoso.com'
        ```

    1. สร้างแอปพลิเคชัน Azure Active Directory (Azure AD) ใหม่ ที่จะเปิดใช้งานบริการ Alm Orchestration เพื่อสื่อสารกับบริการ Scale Unit Management service

        ```powershell
        # Example .\Create-SumAADApplication.ps1 -ConfigurationFilePath ..\ConfigTemplate.xml -TenantId '6240a19e-86f1-41af-91ab-dbe29dbcfb95' -ApplicationDisplayName 'EdgeAgent-SUMCommunication-EN01'
        .\Create-SumAADApplication.ps1 -ConfigurationFilePath '<Path of the ConfigTemplate.xml file>' `
                                       -TenantId '<ID of the tenant where your cloud hub is deployed>' `
                                       -ApplicationDisplayName '<Whichever name you want the Azure AD app to have>'
        ```

1. ทำตามคำแนะนำอย่างต่อเนื่องใน [ตั้งค่าและปรับใช้สภาพแวดล้อมในสถานที่ (Platform update 41 และรุ่นที่ใหม่กว่า)](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md) เมื่อคุณต้องป้อนค่าคอนฟิกสำหรับตัวแทนท้องถิ่น ตรวจสอบให้แน่ใจว่าคุณเปิดใช้งาน Edge Scale Unit Features และระบุพารามิเตอร์ที่จำเป็นครบทั้งหมด

    ![เปิดใช้งาน Edge Scale Unit Features.](media/EnableEdgeScaleUnitFeatures.png "เปิดใช้งาน Edge Scale Unit Features.")

1. ก่อนที่คุณจะปรับใช้สภาพแวดล้อมของคุณจาก LCS ให้ตั้งค่าสคริปต์ก่อนการปรับใช้ สำหรับข้อมูลเพิ่มเติม ดูที่ [สคริปต์ก่อนการปรับใช้และหลังการปรับใช้เอเจนต์ภายใน](../../fin-ops-core/dev-itpro/lifecycle-services/pre-post-scripts.md)

    1. คัดลอกสคริปต์ Configure-CloudAndEdge.ps1 จากโฟลเดอร์ **ScaleUnit** ใน **Infrastructure Scripts** ไปยังโฟลเดอร์ **Scripts** ในที่แบ่งใช้หน่วยจัดเก็บไฟล์ของเอเจนต์ที่ตั้งค่าในสภาพแวดล้อม พาธทั่วไปคือ \\\\lbdiscsi01\\agent\\Scripts
    2. สร้างสคริปต์ **PreDeployment.ps1** ที่จะเรียกสคริปต์โดยใช้พารามิเตอร์ที่จำเป็น ต้องวางสคริปต์การปรับใช้ล่วงหน้าในโฟลเดอร์ **สคริปต์** ในการแบ่งใช้หน่วยจัดเก็บไฟล์ของตัวแทน มิฉะนั้นจะรันไม่ได้ พาธทั่วไปคือ \\\\lbdiscsi01\\agent\\Scripts\\PreDeployment.ps1

        เนื้อหาของสคริปต์ PreDeployment.ps1 จะคล้ายกับตัวอย่างต่อไปนี้

        ```powershell
        $agentShare = '\\lbdiscsi01\agent'
        
        Write-Output "AgentShare is set to $agentShare" 
        . $PSScriptRoot\Configure-CloudAndEdge.ps1 -AgentShare $agentShare -InstanceId '@A'
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
1. หลังจากสภาพแวดล้อมของคุณได้รับการปรับใช้ ให้ทำตามขั้นตอนเหล่านี้

    1. รันคำสั่ง SQL ต่อไปนี้บนฐานข้อมูลธุรกิจของคุณ (AXDB)

        ```sql
        ALTER TABLE dbo.NUMBERSEQUENCETABLE ENABLE CHANGE_TRACKING WITH (TRACK_COLUMNS_UPDATED = ON)
        delete from NumberSequenceTable
        delete from NumberSequenceReference
        delete from NumberSequenceScope
        delete from FeatureManagementMetadata
        delete from FeatureManagementState
        delete from SysFeatureStateV0
        ```

    1. เพิ่มรอบเวลาชุดงานสูงสุดที่เกิดขึ้นพร้อมกันเป็นค่าที่มากกว่า 4

        ```sql
        Update batchserverconfig set maxbatchsessions = '<Replace with number of concurrent batch tasks you want>'
        ```

    1. ตรวจสอบว่าได้เปิดใช้งานการติดตามการเปลี่ยนแปลงในฐานข้อมูลธุรกิจของคุณ (AXDB) แล้ว

        1. เปิดใช้งาน SQL Server Management Studio (SSMS)
        1. เลือกและกด (หรือคลิกขวา) ค้างไว้ที่ฐานข้อมูลธุรกิจของคุณ แล้วเลือก **คุณสมบัติ**
        1. ในหน้าต่างที่ปรากฎ ให้เลือก **การติดตามการเปลี่ยนแปลง** และตั้งค่าต่อไปนี้:

            - **การติดตามการเปลี่ยนแปลง:** *จริง*
            - **รอบระยะเวลาการคงไว้:** *7*
            - **หน่วยการคงไว้:** *วัน*
            - **การล้างข้อมูลอัตโนมัติ:** *จริง*

    1. เพิ่มรหัสแอปพลิเคชัน AD FS ที่คุณสร้างไว้ก่อนหน้านี้ (โดยใช้สคริปต์ Create-ADFSServerApplicationForEdgeScaleUnits.ps1) ลงในตารางแอปพลิเคชัน Azure AD ในหน่วยปรับขนาดของคุณ คุณสามารถดำเนินการขั้นตอนนี้ให้สำเร็จได้ด้วยตนเองผ่านอินเทอร์เฟสผู้ใช้ (UI) หรือคุณสามารถกรอกข้อมูลในฐานข้อมูลได้โดยใช้สคริปต์ต่อไปนี้

        ```sql
        DECLARE @ALMOrchestratorId NVARCHAR(76) = '<Replace with the ADFS Application ID created in a previous step>';

        IF NOT EXISTS (SELECT TOP 1 1 FROM SysAADClientTable WHERE AADClientId = @ALMOrchestratorId)
        BEGIN
            INSERT INTO SysAADClientTable (AADClientId, UserId, Name, ModifiedBy, CreatedBy)
            VALUES (@ALMOrchestratorId, 'ScaleUnitManagement', 'Scale Unit Management', 'Admin', 'Admin');
        END
        ```

## <a name="set-up-an-azure-key-vault-and-an-azure-ad-application-to-enable-communication-between-scale-units"></a><a name="set-up-keyvault"></a>ตั้งค่า Azure key azure และแอปพลิเคชัน Azure AD เพื่อเปิดใช้งานการสื่อสารระหว่างหน่วยปรับขนาด

1. หลังจากสภาพแวดล้อมของคุณได้รับการปรับใช้แล้ว ให้สร้างแอปพลิเคชัน Azure AD เพิ่มเติมเพื่อเปิดใช้งานการสื่อสารที่เชื่อถือได้ระหว่างฮับและหน่วยปรับขนาดของคุณ

    ```powershell
    .\Create-SpokeToHubAADApplication.ps1 -ConfigurationFilePath '<Path of the ConfigTemplate.xml file>' `
                                          -TenantId '<ID of the tenant where your cloud hub is deployed>' `
                                          -ApplicationDisplayName '<Whichever name you want the Azure AD app to have>'
    ```

1. หลังจากสร้างแอปพลิเคชันแล้ว คุณต้องสร้างข้อมูลลับของไคลเอนต์และบันทึกข้อมูลนั้นไว้ในคีย์ Azure นอกจากนี้ คุณต้องให้สิทธิการเข้าถึงแอปพลิเคชัน Azure AD ที่สร้างขึ้น เพื่อให้สามารถดึงข้อมูลลับที่จัดเก็บอยู่ในคีย์ เพื่อความสะดวกของคุณ สคริปต์ต่อไปนี้จะดำเนินการตามขั้นตอนที่จำเป็นทั้งหมดโดยอัตโนมัติ

    ```powershell
    .\Create-SpokeToHubAADAppSecrets.ps1 -ConfigurationFilePath '<Path of the ConfigTemplate.xml file>' `
                                         -TenantId '<ID of the tenant where your cloud hub is deployed>' `
                                         -SubscriptionName '<Any subscription within your tenant>' `
                                         -ResourceGroupName '<Any resource group within your subscription>' `
                                         -KeyVaultName '<Any key vault within your resource group>' `
                                         -Location '<Any Azure location where Azure Key Vault is available>' `
                                         -LCSEnvironmentId '<The LCS environment ID of your deployed scale unit>' `
    ```

    > [!NOTE]
    > ถ้าไม่มีคีย์ที่กำหนดค่า **KeyVaultName** อยู่ สคริปต์จะสร้างค่านั้นโดยอัตโนมัติ

1. เพิ่มรหัสแอปพลิเคชัน Azure AD ที่คุณเพิ่งสร้างขึ้น (เมื่อใช้สคริปต์ Create-HubToHubAADApplication.ps1) ลงในตารางแอปพลิเคชัน Azure AD ในฮับของคุณ คุณสามารถดำเนินการขั้นตอนนี้ให้สำเร็จได้ด้วยตนเองผ่าน UI

## <a name="upload-target-packages-into-lbd-project-assets-in-lcs"></a><a name="upload-packages"></a>อัปโหลดแพคเกจเป้าหมายไปยังสินทรัพย์โครงการ LBD ใน LCS

ขั้นตอนนี้จัดเตรียมเวอร์ชันแอปพลิเคชัน เวอร์ชันแพลตฟอร์ม และการเลือกกำหนดที่จะเปลี่ยนเป็นสภาพแวดล้อมสเกลยูนิต LBD ของคุณ

1. อัปโหลดแพคเกจแอปพลิเคชัน/แพลตฟอร์มรวมเดียวกันกับที่ใช้กับสภาพแวดล้อมฮับ ไปยังไลบรารีสินทรัพย์ของโครงการ LCS ในองค์กร
1. รับสำเนาของแพคเกจที่ปรับใช้แบบกำหนดเองที่ใช้กับสภาพแวดล้อมฮับ และอัปโหลดไปยังไลบรารีสินทรัพย์ของโครงการ LCS ในองค์กร

## <a name="service-the-lbd-environment-with-target-packages"></a><a name="service-target-packages"></a>บริการสภาพแวดล้อม LBD ด้วยแพคเกจเป้าหมาย

ขั้นตอนนี้จัดเรียงเวอร์ชันแอปพลิเคชัน เวอร์ชันแพลตฟอร์ม และการเลือกกำหนดในสภาพแวดล้อมสเกลยูนิต LBD ของคุณด้วยฮับ

1. บริการสภาพแวดล้อม LBD ด้วยแพคเกจแอปพลิเคชัน/แพลตฟอร์มรวมที่คุณอัปโหลดในขั้นตอนก่อนหน้านี้
1. บริการสภาพแวดล้อม LBD ด้วยแพคเกจที่ปรับใช้แบบกำหนดเองที่คุณอัปโหลดในขั้นตอนก่อนหน้านี้

    ![การใช้การอัปเดตใน LCS](media/cloud_edge-LBD-LCS-ServiceLBDEnv1.png "การใช้การอัปเดตใน LCS")

    ![การเลือกแพคเกจการเลือกกำหนดของคุณ](media/cloud_edge-LBD-LCS-ServiceLBDEnv2.png "การเลือกแพคเกจการเลือกกำหนดของคุณ")

## <a name="assign-your-lbd-edge-scale-unit-to-a-hub"></a><a name="assign-edge-to-hub"></a>กําหนดสเกลยูนิตแบบปลายทาง LBD ของคุณให้กับฮับ

คุณตั้งค่าคอนฟิกและจัดการหน่วยการปรับขนาดขอบของคุณผ่าน Scale Unit Management Portal หากต้องการข้อมูลเพิ่มเติม ดูที่ [จัดการหน่วยปรับขนาดและปริมาณงานโดยใช้ Scale Unit Manager portal](./cloud-edge-landing-page.md#scale-unit-manager-portal)

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
