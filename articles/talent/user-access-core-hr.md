---
title: ผู้ใช้สามารถเข้าถึง Core HR ได้ แต่ไม่ใช่แอป Onboard หรือ Attract
description: หัวข้อนี้อธิบายวิธีการแก้ปัญหาที่ซึ่งผู้ใช้สามารถเข้าถึง Microsoft Dynamics 365 for Talent Core HR แต่ไม่สามารถเข้าถึง Attract หรือแอป Onboard ได้
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
ms.openlocfilehash: ece6a81c54ef1421284fc79ab82ed3e31a972255
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/19/2019
ms.locfileid: "855667"
---
# <a name="user-can-access-core-hr-but-not-the-onboard-or-attract-app"></a><span data-ttu-id="1723d-103">ผู้ใช้สามารถเข้าถึง Core HR ได้ แต่ไม่สามารถเข้าถึงแอป Onboard หรือ Attract ได้</span><span class="sxs-lookup"><span data-stu-id="1723d-103">User can access Core HR but not the Onboard or Attract app</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1723d-104">**รายละเอียดสภาพแวดล้อม**</span><span class="sxs-lookup"><span data-stu-id="1723d-104">**Environment details**</span></span>

- <span data-ttu-id="1723d-105">การปรับใช้ผ่าน Microsoft Dynamics Lifecycle Services (LCS) ถูกดำเนินการโดยผู้ใช้ A</span><span class="sxs-lookup"><span data-stu-id="1723d-105">The Microsoft Dynamics Lifecycle Services (LCS) deployment was done by user A.</span></span>
- <span data-ttu-id="1723d-106">ผู้ใช้ A เพิ่มผู้ใช้ B เป็นผู้ใช้ไปยัง Microsoft Dynamics 365 for Talent Core HR</span><span class="sxs-lookup"><span data-stu-id="1723d-106">User A added user B as a user to Microsoft Dynamics 365 for Talent Core HR.</span></span>

<span data-ttu-id="1723d-107">**ออกใช้**</span><span class="sxs-lookup"><span data-stu-id="1723d-107">**Issue**</span></span>

<span data-ttu-id="1723d-108">ผู้ใช้ B สามารถเข้าถึง Core HR ได้ แต่ไม่สามารถเข้าถึง Talent: Attract หรือ Talent: แอป Onboard ได้</span><span class="sxs-lookup"><span data-stu-id="1723d-108">User B can access Core HR, but can't access the Talent: Attract or Talent: Onboard app.</span></span> <span data-ttu-id="1723d-109">เมื่อผู้ใช้พยายามไปยัง **แอปประสบการณ์** เขาหรือเธอจะถูกนำไปยังสภาพแวดล้อมการทดลองแทน</span><span class="sxs-lookup"><span data-stu-id="1723d-109">When the user tries to go to **Experience apps**, he or she is taken to a trial environment instead.</span></span>

<span data-ttu-id="1723d-110">**โซลูชัน**</span><span class="sxs-lookup"><span data-stu-id="1723d-110">**Solution**</span></span>

<span data-ttu-id="1723d-111">ผู้ใช้ B ต้องได้รับมอบหมายสิทธิ์เพื่อดูสภาพแวดล้อม Microsoft PowerApps ที่ผู้ใช้ A สร้างในระหว่างกระบวนการการจัดเตรียม</span><span class="sxs-lookup"><span data-stu-id="1723d-111">User B must be assigned the rights to view the Microsoft PowerApps environment that user A created during the provisioning process.</span></span>

<span data-ttu-id="1723d-112">สำหรับข้อมูล ให้ดูส่วน "การอนุญาตให้เข้าถึงสภาพแวดล้อม" ใน [Talent การเตรียมใช้งาน](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent)</span><span class="sxs-lookup"><span data-stu-id="1723d-112">For information, see the "Granting access to the environment" section in [Provision Talent](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).</span></span>

<span data-ttu-id="1723d-113">**วิธีแก้ปัญหาระยะยาว**</span><span class="sxs-lookup"><span data-stu-id="1723d-113">**Long-term solution**</span></span>

<span data-ttu-id="1723d-114">Microsoft กำลังพิจารณาการกำหนดสิทธิ์ที่เหมาะสมให้กับ Onboard และ Attract โดยอัตโนมัติ เมื่อผู้ใช้ถูกเพิ่มลงใน Core HR</span><span class="sxs-lookup"><span data-stu-id="1723d-114">Microsoft is considering automatically assigning the appropriate rights to Onboard and Attract when a user is added to Core HR.</span></span>
