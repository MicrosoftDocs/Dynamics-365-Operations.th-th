---
title: ผู้ใช้สามารถเข้าถึง Core HR ได้แต่ไม่สามารถเข้าถึง Onboard หรือ Attract ได้
description: หัวข้อนี้อธิบายวิธีการแก้ปัญหาที่ซึ่งผู้ใช้สามารถเข้าถึง Microsoft Dynamics 365 Talent - Core HR แต่ไม่สามารถเข้าถึง Attract หรือ Onboard ได้
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
ms.openlocfilehash: 1a86936d756d8375761ce50c9d9bf33dc638dfad
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772930"
---
# <a name="user-can-access-core-hr-but-not-onboard-or-attract"></a><span data-ttu-id="0c8c9-103">ผู้ใช้สามารถเข้าถึง Core HR ได้แต่ไม่สามารถเข้าถึง Onboard หรือ Attract ได้</span><span class="sxs-lookup"><span data-stu-id="0c8c9-103">User can access Core HR but not Onboard or Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0c8c9-104">**รายละเอียดสภาพแวดล้อม**</span><span class="sxs-lookup"><span data-stu-id="0c8c9-104">**Environment details**</span></span>

- <span data-ttu-id="0c8c9-105">การปรับใช้ผ่าน Microsoft Dynamics Lifecycle Services (LCS) ถูกดำเนินการโดยผู้ใช้ A</span><span class="sxs-lookup"><span data-stu-id="0c8c9-105">The Microsoft Dynamics Lifecycle Services (LCS) deployment was done by user A.</span></span>
- <span data-ttu-id="0c8c9-106">ผู้ใช้ A เพิ่มผู้ใช้ B เป็นผู้ใช้ไปยัง Microsoft Dynamics 365 Talent: Core HR</span><span class="sxs-lookup"><span data-stu-id="0c8c9-106">User A added user B as a user to Microsoft Dynamics 365 Talent: Core HR.</span></span>

<span data-ttu-id="0c8c9-107">**ออกใช้**</span><span class="sxs-lookup"><span data-stu-id="0c8c9-107">**Issue**</span></span>

<span data-ttu-id="0c8c9-108">ผู้ใช้ B สามารถเข้าถึง Core HR ได้ แต่ไม่สามารถเข้าถึง Talent: Attract หรือ Talent: แอป Onboard ได้</span><span class="sxs-lookup"><span data-stu-id="0c8c9-108">User B can access Core HR, but can't access the Talent: Attract or Talent: Onboard app.</span></span> <span data-ttu-id="0c8c9-109">เมื่อผู้ใช้พยายามไปยัง **แอปประสบการณ์** เขาหรือเธอจะถูกนำไปยังสภาพแวดล้อมการทดลองแทน</span><span class="sxs-lookup"><span data-stu-id="0c8c9-109">When the user tries to go to **Experience apps**, he or she is taken to a trial environment instead.</span></span>

<span data-ttu-id="0c8c9-110">**โซลูชัน**</span><span class="sxs-lookup"><span data-stu-id="0c8c9-110">**Solution**</span></span>

<span data-ttu-id="0c8c9-111">ผู้ใช้ B ต้องได้รับมอบหมายสิทธิ์เพื่อดูสภาพแวดล้อม Microsoft Power Apps ที่ผู้ใช้ A สร้างในระหว่างกระบวนการการจัดเตรียม</span><span class="sxs-lookup"><span data-stu-id="0c8c9-111">User B must be assigned the rights to view the Microsoft Power Apps environment that user A created during the provisioning process.</span></span>

<span data-ttu-id="0c8c9-112">สำหรับข้อมูล ให้ดูส่วน "การอนุญาตให้เข้าถึงสภาพแวดล้อม" ใน [Talent การเตรียมใช้งาน](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent)</span><span class="sxs-lookup"><span data-stu-id="0c8c9-112">For information, see the "Granting access to the environment" section in [Provision Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span></span>

<span data-ttu-id="0c8c9-113">**วิธีแก้ปัญหาระยะยาว**</span><span class="sxs-lookup"><span data-stu-id="0c8c9-113">**Long-term solution**</span></span>

<span data-ttu-id="0c8c9-114">Microsoft กำลังพิจารณาการกำหนดสิทธิ์ที่เหมาะสมให้กับ Onboard และ Attract โดยอัตโนมัติ เมื่อผู้ใช้ถูกเพิ่มลงใน Core HR</span><span class="sxs-lookup"><span data-stu-id="0c8c9-114">Microsoft is considering automatically assigning the appropriate rights to Onboard and Attract when a user is added to Core HR.</span></span>
