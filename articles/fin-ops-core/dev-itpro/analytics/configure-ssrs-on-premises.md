---
title: ตั้งค่าคอนฟิก SQL Server Reporting Services สำหรับการปรับใช้แบบ on-premises
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับการตั้งค่าคอนฟิกบริการรายงาน SQL Server (SSRS) สำหรับการปรับใช้ในองค์กร
author: PeterRFriis
ms.date: 06/23/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 55651
ms.assetid: ''
ms.search.region: Global
ms.author: peterfriis
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.openlocfilehash: 88e6d5470ff7808a9b6263b6426e19f6ea11493d
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755535"
---
# <a name="configure-sql-server-reporting-services-for-on-premises-deployments"></a><span data-ttu-id="bde5d-103">ตั้งค่าคอนฟิก SQL Server Reporting Services สำหรับการปรับใช้แบบ on-premises</span><span class="sxs-lookup"><span data-stu-id="bde5d-103">Configure SQL Server Reporting Services for on-premises deployments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bde5d-104">ใช้ขั้นตอนในหัวข้อนี้เพื่อตั้งค่าคอนฟิก SQL Server Reporting Services (SSRS) สำหรับการปรับใช้ Microsoft Dynamics 365 Finance + Operations (on-premises) ของคุณ</span><span class="sxs-lookup"><span data-stu-id="bde5d-104">Use the steps in this topic to configure SQL Server Reporting Services (SSRS) for your Microsoft Dynamics 365 Finance + Operations (on-premises) deployment.</span></span>

1. <span data-ttu-id="bde5d-105">เปิดแอพลิเคชัน Reporting Services Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="bde5d-105">Open the Reporting Services Configuration Manager application.</span></span>
2. <span data-ttu-id="bde5d-106">ทิ้ง **ชื่อเซิร์ฟเวอร์** เริ่มต้น ซึ่งควรเป็นชื่อของเครื่องปัจจุบัน และ **อินสแตนซ์ของเซิร์ฟเวอร์รายงาน** **MSSQLSERVER**</span><span class="sxs-lookup"><span data-stu-id="bde5d-106">Leave the default **Server name**, which should be the name of the current machine, and the **Report Server Instance**, **MSSQLSERVER**.</span></span>
3. <span data-ttu-id="bde5d-107">คลิก **เชื่อมต่อ**</span><span class="sxs-lookup"><span data-stu-id="bde5d-107">Click **Connect**.</span></span>

    <span data-ttu-id="bde5d-108">[![การเชื่อมต่อการตั้งค่าคอนฟิกเซิร์ฟเวอร์การรายงาน](./media/ssrs-config-manager-01.png)](./media/ssrs-config-manager-01.png)</span><span class="sxs-lookup"><span data-stu-id="bde5d-108">[![Reporting services configuration connection](./media/ssrs-config-manager-01.png)](./media/ssrs-config-manager-01.png)</span></span>

4. <span data-ttu-id="bde5d-109">คลิกแท็บ **บัญชีบริการ** และตรวจสอบว่าการตั้งค่าตรงกับภาพต่อไปนี้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="bde5d-109">Click the **Service Account** tab and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="bde5d-110">[![แท็บบัญชีบริการ](./media/ssrs-config-manager-02.png)](./media/ssrs-config-manager-02.png)</span><span class="sxs-lookup"><span data-stu-id="bde5d-110">[![Service account tab](./media/ssrs-config-manager-02.png)](./media/ssrs-config-manager-02.png)</span></span>

5. <span data-ttu-id="bde5d-111">คลิกแท็บ **URL ของเว็บเซอร์วิส** และตรวจสอบว่าการตั้งค่าตรงกับภาพต่อไปนี้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="bde5d-111">Click the **Web Service URL** tab and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="bde5d-112">[![แท็บ URL ของบริการเว็บ](./media/ssrs-config-manager-03.png)](./media/ssrs-config-manager-03.png)</span><span class="sxs-lookup"><span data-stu-id="bde5d-112">[![Web service URL tab](./media/ssrs-config-manager-03.png)](./media/ssrs-config-manager-03.png)</span></span>

6. <span data-ttu-id="bde5d-113">คลิกแท็บ **ฐานข้อมูล** และตรวจสอบว่า **ชื่อฐานข้อมูล** และ **การตั้งค่าข้อมูลประจำตัว** ตรงกับภาพต่อไปนี้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="bde5d-113">Click the **Database** tab and verify that the **Database Name** and **Credential settings** match the following graphic.</span></span>

    > [!NOTE]
    > <span data-ttu-id="bde5d-114">คุณจะต้องสร้างฐานข้อมูลใหม่</span><span class="sxs-lookup"><span data-stu-id="bde5d-114">You will need to create a new database.</span></span> <span data-ttu-id="bde5d-115">เมื่อต้องการทำเช่นนี้ ให้คลิก **เปลี่ยนแปลงฐานข้อมูล** แล้วตรวจสอบว่าชื่อฐานข้อมูลใหม่คือ: **DynamicsAxReportServer**</span><span class="sxs-lookup"><span data-stu-id="bde5d-115">To do this, click **Change Database**, and then verify that the new database name is: **DynamicsAxReportServer**.</span></span>

    <span data-ttu-id="bde5d-116">[![แท็บฐานข้อมูล](./media/ssrs-config-manager-04.png)](./media/ssrs-config-manager-04.png)</span><span class="sxs-lookup"><span data-stu-id="bde5d-116">[![database tab](./media/ssrs-config-manager-04.png)](./media/ssrs-config-manager-04.png)</span></span>

7. <span data-ttu-id="bde5d-117">คลิกแท็บ **URL ของเว็บพอร์ทัล** และตรวจสอบว่าการตั้งค่าตรงกับภาพต่อไปนี้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="bde5d-117">Click the **Web Portal URL** tab and verify that the settings match the following graphic.</span></span>

    > [!NOTE]
    > <span data-ttu-id="bde5d-118">คุณต้องคลิก **ใช้** เพื่อสร้างและตั้งค่าคอนฟิกพอร์ทัลให้ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="bde5d-118">You must click **Apply** to create and properly configure the Portal.</span></span>

    <span data-ttu-id="bde5d-119">[![แท็บ URL ของเว็บพอร์ทัล](./media/ssrs-config-manager-05.png)](./media/ssrs-config-manager-05.png)</span><span class="sxs-lookup"><span data-stu-id="bde5d-119">[![web portal url tab](./media/ssrs-config-manager-05.png)](./media/ssrs-config-manager-05.png)</span></span>

    <span data-ttu-id="bde5d-120">หลังจากที่มีการตั้งค่าคอนฟิกพอร์ทัล แท็บ **เว็บพอร์ทัล** จะตรงกับรูปภาพต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="bde5d-120">After the Portal is configured, the **Web Portal** tab will match the following graphic.</span></span>

    <span data-ttu-id="bde5d-121">[![แท็บเว็บพอร์ทัล](./media/ssrs-config-manager-06.png)](./media/ssrs-config-manager-06.png)</span><span class="sxs-lookup"><span data-stu-id="bde5d-121">[![web portal tab](./media/ssrs-config-manager-06.png)](./media/ssrs-config-manager-06.png)</span></span>

8. <span data-ttu-id="bde5d-122">คลิก URL รายงานเพื่อดูเว็บพอร์ทัลบริการรายงาน SQL Server</span><span class="sxs-lookup"><span data-stu-id="bde5d-122">Click the reports URL to view the SQL Server Reporting Services web portal.</span></span>
9. <span data-ttu-id="bde5d-123">เมื่อคุณอยู่ในพอร์ทัล ให้สร้างโฟลเดอร์ใหม่ที่ชื่อว่า **Dynamics**</span><span class="sxs-lookup"><span data-stu-id="bde5d-123">When you are in the portal, create a new folder named **Dynamics**.</span></span>

    <span data-ttu-id="bde5d-124">[![โฟลเดอร์ Dynamics](./media/ssrs-config-manager-07.png)](./media/ssrs-config-manager-07.png)</span><span class="sxs-lookup"><span data-stu-id="bde5d-124">[![dynamics folder](./media/ssrs-config-manager-07.png)](./media/ssrs-config-manager-07.png)</span></span>

10. <span data-ttu-id="bde5d-125">ใน **Reporting Services Configuration Manager** คลิกแท็บ **การตั้งค่าอีเมล** และตรวจสอบว่าการตั้งค่าตรงกับภาพต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="bde5d-125">In the **Reporting Services Configuration Manager**, click the **E-mail Settings** tab and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="bde5d-126">[![แท็บการตั้งค่าอีเมล](./media/ssrs-config-manager-08.png)](./media/ssrs-config-manager-08.png)</span><span class="sxs-lookup"><span data-stu-id="bde5d-126">[![email settings tab](./media/ssrs-config-manager-08.png)](./media/ssrs-config-manager-08.png)</span></span>

11. <span data-ttu-id="bde5d-127">คลิกแท็บ **บัญชีการดำเนินการ** และตรวจสอบว่าการตั้งค่าตรงกับภาพต่อไปนี้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="bde5d-127">Click the **Execution Account** tab and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="bde5d-128">[![แท็บบัญชีการดำเนินการ](./media/ssrs-config-manager-09.png)](./media/ssrs-config-manager-09.png)</span><span class="sxs-lookup"><span data-stu-id="bde5d-128">[![execution account tab](./media/ssrs-config-manager-09.png)](./media/ssrs-config-manager-09.png)</span></span>

    <span data-ttu-id="bde5d-129">อย่าเปลี่ยนการตั้งค่าเริ่มต้นบนแท็บ **คีย์การเข้ารหัส**</span><span class="sxs-lookup"><span data-stu-id="bde5d-129">Don't change the default settings on the **Encryption Keys** tab.</span></span>

    <span data-ttu-id="bde5d-130">[![แท็บคีย์การเข้ารหัส](./media/ssrs-config-manager-10.png)](./media/ssrs-config-manager-10.png)</span><span class="sxs-lookup"><span data-stu-id="bde5d-130">[![encryption keys tab](./media/ssrs-config-manager-10.png)](./media/ssrs-config-manager-10.png)</span></span>

12. <span data-ttu-id="bde5d-131">คลิกแท็บ **การตั้งค่าการบอกรับเป็นสมาชิก** และตรวจสอบว่าการตั้งค่าตรงกับภาพต่อไปนี้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="bde5d-131">Click the **Subscription Settings** tab, and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="bde5d-132">[![แท็บการตั้งค่าการบอกรับเป็นสมาชิก](./media/ssrs-config-manager-11.png)](./media/ssrs-config-manager-11.png)</span><span class="sxs-lookup"><span data-stu-id="bde5d-132">[![subscription settings tab](./media/ssrs-config-manager-11.png)](./media/ssrs-config-manager-11.png)</span></span>

    <span data-ttu-id="bde5d-133">อย่าเปลี่ยนการตั้งค่าเริ่มต้นบนแท็บ **การปรับใช้ Scale-out**</span><span class="sxs-lookup"><span data-stu-id="bde5d-133">Don't change the default settings on the **Scale-out Deployment** tab.</span></span>

    <span data-ttu-id="bde5d-134">[![แท็บการปรับใช้ Scale-out](./media/ssrs-config-manager-12.png)](./media/ssrs-config-manager-12.png)</span><span class="sxs-lookup"><span data-stu-id="bde5d-134">[![scale-out deployment tab](./media/ssrs-config-manager-12.png)](./media/ssrs-config-manager-12.png)</span></span>

    <span data-ttu-id="bde5d-135">ห้ามเปลี่ยนการตั้งค่าเริ่มต้นบนแท็บ **การรวม Power BI**</span><span class="sxs-lookup"><span data-stu-id="bde5d-135">Don't change the default settings on the **Power BI Integration** tab.</span></span>

    <span data-ttu-id="bde5d-136">[![แท็บการรวม power bi](./media/ssrs-config-manager-13.png)](./media/ssrs-config-manager-13.png)</span><span class="sxs-lookup"><span data-stu-id="bde5d-136">[![power bi integration tab](./media/ssrs-config-manager-13.png)](./media/ssrs-config-manager-13.png)</span></span>

13. <span data-ttu-id="bde5d-137">คลิก **ออก** เพื่อปิด **Reporting Services Configuration Manager**</span><span class="sxs-lookup"><span data-stu-id="bde5d-137">Click **Exit** to close the **Reporting Services Configuration Manager**.</span></span>

    <span data-ttu-id="bde5d-138">[![ปิด Reporting Services Configuration Manager](./media/ssrs-config-manager-14.png)](./media/ssrs-config-manager-14.png)</span><span class="sxs-lookup"><span data-stu-id="bde5d-138">[![close reporting services configuration manager](./media/ssrs-config-manager-14.png)](./media/ssrs-config-manager-14.png)</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
