---
title: ทรัพยากรบุคคลไม่มีอยู่ในแอป Microsoft Dynamics 365
description: บทความนี้อธิบายถึงสิ่งที่ต้องทำ ถ้าลูกค้าไม่เห็นแอป Microsoft Dynamics 365 Human Resources ระหว่างแอป Microsoft Dynamics 365
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 658c6a4f17c022c3d0e3e49d16eb89624c4be27c
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5803980"
---
# <a name="human-resources-doesnt-appear-in-microsoft-dynamics-365-apps"></a><span data-ttu-id="a5b47-103">ทรัพยากรบุคคลไม่มีอยู่ในแอป Microsoft Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="a5b47-103">Human Resources doesn't appear in Microsoft Dynamics 365 apps</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="a5b47-104">**ออกใช้**</span><span class="sxs-lookup"><span data-stu-id="a5b47-104">**Issue**</span></span>

<span data-ttu-id="a5b47-105">ลูกค้าไม่เห็น Dynamics 365 Human Resources ในแอป Microsoft Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="a5b47-105">The customer doesn't see Dynamics 365 Human Resources among the Microsoft Dynamics 365 apps.</span></span>

<span data-ttu-id="a5b47-106">**ความละเอียด**</span><span class="sxs-lookup"><span data-stu-id="a5b47-106">**Resolution**</span></span>

<span data-ttu-id="a5b47-107">ต้องมีการเพิ่มผู้ใช้ให้กับบทบาทผู้สร้างสภาพแวดล้อมสำหรับสภาพแวดล้อมใน Microsoft Power Apps</span><span class="sxs-lookup"><span data-stu-id="a5b47-107">The user must be added to the Environment Maker role for the environment in Microsoft Power Apps.</span></span>

1. <span data-ttu-id="a5b47-108">ผู้ใช้ที่เป็นผู้ดูแลระบบที่มีลิขสิทธิ์ Power Apps Plan 2 ต้องเปิด [พอร์ทัลผู้ดูแลระบบ Power Apps](https://preview.admin.powerapps.com/)</span><span class="sxs-lookup"><span data-stu-id="a5b47-108">The admin user who has a Power Apps Plan 2 license must open the [Power Apps Admin portal](https://preview.admin.powerapps.com/).</span></span>

2. <span data-ttu-id="a5b47-109">เลือก **สภาพแวดล้อม** และเลือกสภาพแวดล้อมที่ถูกต้องสำหรับทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="a5b47-109">Select **Environments**, and select the correct environment for Human Resources.</span></span>

3. <span data-ttu-id="a5b47-110">บนแท็บ **ความปลอดภัย** บนแท็บ **บทบาทสภาพแวดล้อม** เลือก **ผู้ผู้สร้างสภาพแวดล้อม**</span><span class="sxs-lookup"><span data-stu-id="a5b47-110">On the **Security** tab, on the **Environment roles** tab, select **Environment Maker**.</span></span>

    ![แท็บบทบาทสภาพแวดล้อม](media/environment-roles.png)

4. <span data-ttu-id="a5b47-112">บนแท็บ **ผู้ใช้** เพิ่มผู้ใช้หรือองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="a5b47-112">On the **Users** tab, add the user or your organization.</span></span>

    ![แท็บผู้ใช้](media/environment-maker.png)

5. <span data-ttu-id="a5b47-114">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="a5b47-114">Select **Save**.</span></span>

6. <span data-ttu-id="a5b47-115">ขณะนี้ ผู้ใช้ต้องลงชื่อเข้าใช้ใน [Microsoft Dynamics 365](https://home.dynamics.com/)</span><span class="sxs-lookup"><span data-stu-id="a5b47-115">The user must now sign in to [Microsoft Dynamics 365](https://home.dynamics.com/).</span></span>

7. <span data-ttu-id="a5b47-116">เลือก **ซิงค์** เพื่ออัพเดตแอปผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="a5b47-116">Select **Sync** to update the user apps.</span></span>

    ![ซิงค์ปุ่ม](media/get-more.png)

    <span data-ttu-id="a5b47-118">หลังจากการซิงโครไนส์เสร็จสมบูรณ์ ทรัพยากรบุคคลจะปรากฏขึ้นบนโฮมเพจ</span><span class="sxs-lookup"><span data-stu-id="a5b47-118">After synchronization is completed, Human Resources will appear on the home page.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]