---
title: Talent ไม่ปรากฏขึ้นในแอป Microsoft Dynamics 365 (Common Data Service 1.0)
description: หัวข้อนี้อธิบายถึงสิ่งที่ต้องทำ ถ้าลูกค้าไม่เห็นแอป Microsoft Dynamics 365 for Talent ระหว่างแอป Microsoft Dynamics 365
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: ad5add2b572ccb6bff175806b965f63b53986152
ms.sourcegitcommit: 45b79d1e587e03f5cde2766cdec4eaa7a2a897a3
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/02/2019
ms.locfileid: "949793"
---
# <a name="talent-doesnt-appear-among-the-microsoft-dynamics-365-apps-common-data-service-10"></a><span data-ttu-id="8dddc-103">Talent ไม่ปรากฏขึ้นในแอป Microsoft Dynamics 365 (Common Data Service 1.0)</span><span class="sxs-lookup"><span data-stu-id="8dddc-103">Talent doesn't appear among the Microsoft Dynamics 365 apps (Common Data Service 1.0)</span></span>

[!include [banner](includes/banner.md)]

**<span data-ttu-id="8dddc-104">ออกใช้</span><span class="sxs-lookup"><span data-stu-id="8dddc-104">Issue</span></span>**

<span data-ttu-id="8dddc-105">ลูกค้าจะไม่เห็นแอป Microsoft Dynamics 365 for Talent ระหว่างแอป Microsoft Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="8dddc-105">The customer doesn't see the Microsoft Dynamics 365 for Talent app among the Microsoft Dynamics 365 apps.</span></span>

**<span data-ttu-id="8dddc-106">ความละเอียด</span><span class="sxs-lookup"><span data-stu-id="8dddc-106">Resolution</span></span>**

<span data-ttu-id="8dddc-107">ต้องมีการเพิ่มผู้ใช้ให้กับบทบาทผู้สร้างสภาพแวดล้อมสำหรับสภาพแวดล้อมใน Microsoft PowerApps</span><span class="sxs-lookup"><span data-stu-id="8dddc-107">The user must be added to the Environment Maker role for the environment in Microsoft PowerApps.</span></span>

1. <span data-ttu-id="8dddc-108">ผู้ใช้ที่เป็นผู้ดูแลระบบที่มีลิขสิทธิ์ PowerApps แผน 2 ต้องเปิด [พอร์ทัลผู้ดูแลระบบ PowerApps](https://preview.admin.powerapps.com/)</span><span class="sxs-lookup"><span data-stu-id="8dddc-108">The admin user who has a PowerApps Plan 2 license must open the [PowerApps Admin portal](https://preview.admin.powerapps.com/).</span></span>
2. <span data-ttu-id="8dddc-109">เลือก **สภาพแวดล้อม** และเลือกสภาพแวดล้อมที่ถูกต้องสำหรับ Talent</span><span class="sxs-lookup"><span data-stu-id="8dddc-109">Select **Environments**, and select the correct environment for Talent.</span></span>
3. <span data-ttu-id="8dddc-110">บนแท็บ **ความปลอดภัย** บนแท็บ **บทบาทสภาพแวดล้อม** เลือก **ผู้ผู้สร้างสภาพแวดล้อม**</span><span class="sxs-lookup"><span data-stu-id="8dddc-110">On the **Security** tab, on the **Environment roles** tab, select **Environment Maker**.</span></span>

    ![แท็บบทบาทสภาพแวดล้อม](media/environment-roles.png)

4. <span data-ttu-id="8dddc-112">บนแท็บ **ผู้ใช้** เพิ่มผู้ใช้หรือองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="8dddc-112">On the **Users** tab, add the user or your organization.</span></span>

    ![แท็บผู้ใช้](media/environment-maker.png)

5. <span data-ttu-id="8dddc-114">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="8dddc-114">Select **Save**.</span></span>
6. <span data-ttu-id="8dddc-115">ขณะนี้ ผู้ใช้ต้องลงชื่อเข้าใช้ใน [Microsoft Dynamics 365](https://home.dynamics.com/)</span><span class="sxs-lookup"><span data-stu-id="8dddc-115">The user must now sign in to [Microsoft Dynamics 365](https://home.dynamics.com/).</span></span>
7. <span data-ttu-id="8dddc-116">เลือก **ซิงค์** เพื่ออัพเดตแอปผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="8dddc-116">Select **Sync** to update the user apps.</span></span>

    ![ซิงค์ปุ่ม](media/get-more.png)

    <span data-ttu-id="8dddc-118">หลังจากการซิงโครไนส์เสร็จสมบูรณ์ Talent จะปรากฏขึ้นบนโฮมเพจ</span><span class="sxs-lookup"><span data-stu-id="8dddc-118">After synchronization is completed, Talent will appear on the home page.</span></span>
