---
title: ทรัพยากรบุคคลไม่มีอยู่ในแอป Microsoft Dynamics 365
description: บทความนี้อธิบายถึงสิ่งที่ต้องทำ ถ้าลูกค้าไม่เห็นแอป Microsoft Dynamics 365 Human Resources ระหว่างแอป Microsoft Dynamics 365
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d39e6ef4168f08f20b92979a296ed088744ad0da
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010804"
---
# <a name="human-resources-doesnt-appear-in-microsoft-dynamics-365-apps"></a><span data-ttu-id="caf24-103">ทรัพยากรบุคคลไม่มีอยู่ในแอป Microsoft Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="caf24-103">Human Resources doesn't appear in Microsoft Dynamics 365 apps</span></span>

<span data-ttu-id="caf24-104">**ออกใช้**</span><span class="sxs-lookup"><span data-stu-id="caf24-104">**Issue**</span></span>

<span data-ttu-id="caf24-105">ลูกค้าไม่เห็น Dynamics 365 Human Resources ในแอป Microsoft Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="caf24-105">The customer doesn't see Dynamics 365 Human Resources among the Microsoft Dynamics 365 apps.</span></span>

<span data-ttu-id="caf24-106">**ความละเอียด**</span><span class="sxs-lookup"><span data-stu-id="caf24-106">**Resolution**</span></span>

<span data-ttu-id="caf24-107">ต้องมีการเพิ่มผู้ใช้ให้กับบทบาทผู้สร้างสภาพแวดล้อมสำหรับสภาพแวดล้อมใน Microsoft Power Apps</span><span class="sxs-lookup"><span data-stu-id="caf24-107">The user must be added to the Environment Maker role for the environment in Microsoft Power Apps.</span></span>

1. <span data-ttu-id="caf24-108">ผู้ใช้ที่เป็นผู้ดูแลระบบที่มีลิขสิทธิ์ Power Apps Plan 2 ต้องเปิด [พอร์ทัลผู้ดูแลระบบ Power Apps](https://preview.admin.powerapps.com/)</span><span class="sxs-lookup"><span data-stu-id="caf24-108">The admin user who has a Power Apps Plan 2 license must open the [Power Apps Admin portal](https://preview.admin.powerapps.com/).</span></span>

2. <span data-ttu-id="caf24-109">เลือก **สภาพแวดล้อม** และเลือกสภาพแวดล้อมที่ถูกต้องสำหรับทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="caf24-109">Select **Environments**, and select the correct environment for Human Resources.</span></span>

3. <span data-ttu-id="caf24-110">บนแท็บ **ความปลอดภัย** บนแท็บ **บทบาทสภาพแวดล้อม** เลือก **ผู้ผู้สร้างสภาพแวดล้อม**</span><span class="sxs-lookup"><span data-stu-id="caf24-110">On the **Security** tab, on the **Environment roles** tab, select **Environment Maker**.</span></span>

    ![แท็บบทบาทสภาพแวดล้อม](media/environment-roles.png)

4. <span data-ttu-id="caf24-112">บนแท็บ **ผู้ใช้** เพิ่มผู้ใช้หรือองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="caf24-112">On the **Users** tab, add the user or your organization.</span></span>

    ![แท็บผู้ใช้](media/environment-maker.png)

5. <span data-ttu-id="caf24-114">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="caf24-114">Select **Save**.</span></span>

6. <span data-ttu-id="caf24-115">ขณะนี้ ผู้ใช้ต้องลงชื่อเข้าใช้ใน [Microsoft Dynamics 365](https://home.dynamics.com/)</span><span class="sxs-lookup"><span data-stu-id="caf24-115">The user must now sign in to [Microsoft Dynamics 365](https://home.dynamics.com/).</span></span>

7. <span data-ttu-id="caf24-116">เลือก **ซิงค์** เพื่ออัพเดตแอปผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="caf24-116">Select **Sync** to update the user apps.</span></span>

    ![ซิงค์ปุ่ม](media/get-more.png)

    <span data-ttu-id="caf24-118">หลังจากการซิงโครไนส์เสร็จสมบูรณ์ ทรัพยากรบุคคลจะปรากฏขึ้นบนโฮมเพจ</span><span class="sxs-lookup"><span data-stu-id="caf24-118">After synchronization is completed, Human Resources will appear on the home page.</span></span>
