---
title: Talent ไม่ปรากฏขึ้นในแอป Microsoft Dynamics 365 (CDS1.0)
description: หัวข้อนี้อธิบายถึงสิ่งที่ต้องทำ ถ้าลูกค้าไม่เห็นแอป Microsoft Dynamics 365 for Talent ระหว่างแอป Microsoft Dynamics 365
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 32ae0ab807e953bd811a557e6878b9bee79d293c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "306455"
---
# <a name="talent-doesnt-appear-among-the-microsoft-dynamics-365-apps-cds10"></a><span data-ttu-id="a1538-103">Talent ไม่ปรากฏขึ้นในแอป Microsoft Dynamics 365 (CDS1.0)</span><span class="sxs-lookup"><span data-stu-id="a1538-103">Talent doesn't appear among the Microsoft Dynamics 365 apps (CDS1.0)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a1538-104">**ออกใช้**</span><span class="sxs-lookup"><span data-stu-id="a1538-104">**Issue**</span></span>

<span data-ttu-id="a1538-105">ลูกค้าจะไม่เห็นแอป Microsoft Dynamics 365 for Talent ระหว่างแอป Microsoft Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="a1538-105">The customer doesn't see the Microsoft Dynamics 365 for Talent app among the Microsoft Dynamics 365 apps.</span></span>

<span data-ttu-id="a1538-106">**ความละเอียด**</span><span class="sxs-lookup"><span data-stu-id="a1538-106">**Resolution**</span></span>

<span data-ttu-id="a1538-107">ต้องมีการเพิ่มผู้ใช้ให้กับบทบาทผู้สร้างสภาพแวดล้อมสำหรับสภาพแวดล้อมใน Microsoft PowerApps</span><span class="sxs-lookup"><span data-stu-id="a1538-107">The user must be added to the Environment Maker role for the environment in Microsoft PowerApps.</span></span>

1. <span data-ttu-id="a1538-108">ผู้ใช้ที่เป็นผู้ดูแลระบบที่มีลิขสิทธิ์ PowerApps แผน 2 ต้องเปิด [พอร์ทัลผู้ดูแลระบบ PowerApps](https://preview.admin.powerapps.com/)</span><span class="sxs-lookup"><span data-stu-id="a1538-108">The admin user who has a PowerApps Plan 2 license must open the [PowerApps Admin portal](https://preview.admin.powerapps.com/).</span></span>
2. <span data-ttu-id="a1538-109">เลือก **สภาพแวดล้อม** และเลือกสภาพแวดล้อมที่ถูกต้องสำหรับ Talent</span><span class="sxs-lookup"><span data-stu-id="a1538-109">Select **Environments**, and select the correct environment for Talent.</span></span>
3. <span data-ttu-id="a1538-110">บนแท็บ **ความปลอดภัย** บนแท็บ **บทบาทสภาพแวดล้อม** เลือก **ผู้ผู้สร้างสภาพแวดล้อม**</span><span class="sxs-lookup"><span data-stu-id="a1538-110">On the **Security** tab, on the **Environment roles** tab, select **Environment Maker**.</span></span>

    ![แท็บบทบาทสภาพแวดล้อม](media/environment-roles.png)

4. <span data-ttu-id="a1538-112">บนแท็บ **ผู้ใช้** เพิ่มผู้ใช้หรือองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="a1538-112">On the **Users** tab, add the user or your organization.</span></span>

    ![แท็บผู้ใช้](media/environment-maker.png)

5. <span data-ttu-id="a1538-114">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="a1538-114">Select **Save**.</span></span>
6. <span data-ttu-id="a1538-115">ขณะนี้ ผู้ใช้ต้องลงชื่อเข้าใช้ใน [Microsoft Dynamics 365](https://home.dynamics.com/)</span><span class="sxs-lookup"><span data-stu-id="a1538-115">The user must now sign in to [Microsoft Dynamics 365](https://home.dynamics.com/).</span></span>
7. <span data-ttu-id="a1538-116">เลือก **ซิงค์** เพื่ออัพเดตแอปผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="a1538-116">Select **Sync** to update the user apps.</span></span>

    ![ซิงค์ปุ่ม](media/get-more.png)

    <span data-ttu-id="a1538-118">หลังจากการซิงโครไนส์เสร็จสมบูรณ์ Talent จะปรากฏขึ้นบนโฮมเพจ</span><span class="sxs-lookup"><span data-stu-id="a1538-118">After synchronization is completed, Talent will appear on the home page.</span></span>
