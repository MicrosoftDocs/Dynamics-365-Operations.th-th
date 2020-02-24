---
title: ผู้ใช้สามารถเข้าถึงทรัพยากรบุคคลได้ แต่ไม่สามารถเข้าถึง Onboard หรือ Attract ได้
description: หัวข้อนี้อธิบายวิธีการแก้ปัญหาที่ซึ่งผู้ใช้สามารถเข้าถึง Microsoft Dynamics 365 Talent - ทรัพยากรบุคคลได้ แต่ไม่สามารถเข้าถึง Attract หรือ Onboard ได้
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
ms.openlocfilehash: 6c384d9a7100982eabd201d910e1bea14355dc1f
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/03/2020
ms.locfileid: "3006321"
---
# <a name="user-can-access-human-resources-but-not-onboard-or-attract"></a><span data-ttu-id="365e8-103">ผู้ใช้สามารถเข้าถึงทรัพยากรบุคคลได้ แต่ไม่สามารถเข้าถึง Onboard หรือ Attract ได้</span><span class="sxs-lookup"><span data-stu-id="365e8-103">User can access Human Resources but not Onboard or Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="365e8-104">**รายละเอียดสภาพแวดล้อม**</span><span class="sxs-lookup"><span data-stu-id="365e8-104">**Environment details**</span></span>

- <span data-ttu-id="365e8-105">การปรับใช้ผ่าน Microsoft Dynamics Lifecycle Services (LCS) ถูกดำเนินการโดยผู้ใช้ A</span><span class="sxs-lookup"><span data-stu-id="365e8-105">The Microsoft Dynamics Lifecycle Services (LCS) deployment was done by user A.</span></span>
- <span data-ttu-id="365e8-106">ผู้ใช้ A เพิ่มผู้ใช้ B เป็นผู้ใช้ไปยัง Microsoft Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="365e8-106">User A added user B as a user to Microsoft Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="365e8-107">**ออกใช้**</span><span class="sxs-lookup"><span data-stu-id="365e8-107">**Issue**</span></span>

<span data-ttu-id="365e8-108">ผู้ใช้ B สามารถเข้าถึงทรัพยากรบุคคลได้ แต่ไม่สามารถเข้าถึงแอป Talent: Attract หรือ Talent: Onboard ได้</span><span class="sxs-lookup"><span data-stu-id="365e8-108">User B can access Human Resources, but can't access the Talent: Attract or Talent: Onboard app.</span></span> <span data-ttu-id="365e8-109">เมื่อผู้ใช้พยายามไปยัง **แอปประสบการณ์** เขาหรือเธอจะถูกนำไปยังสภาพแวดล้อมการทดลองแทน</span><span class="sxs-lookup"><span data-stu-id="365e8-109">When the user tries to go to **Experience apps**, he or she is taken to a trial environment instead.</span></span>

<span data-ttu-id="365e8-110">**โซลูชัน**</span><span class="sxs-lookup"><span data-stu-id="365e8-110">**Solution**</span></span>

<span data-ttu-id="365e8-111">ผู้ใช้ B ต้องได้รับมอบหมายสิทธิ์เพื่อดูสภาพแวดล้อม Microsoft Power Apps ที่ผู้ใช้ A สร้างในระหว่างกระบวนการการจัดเตรียม</span><span class="sxs-lookup"><span data-stu-id="365e8-111">User B must be assigned the rights to view the Microsoft Power Apps environment that user A created during the provisioning process.</span></span>

<span data-ttu-id="365e8-112">สำหรับข้อมูล ให้ดูส่วน "การอนุญาตให้เข้าถึงสภาพแวดล้อม" ใน [Talent การเตรียมใช้งาน](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent)</span><span class="sxs-lookup"><span data-stu-id="365e8-112">For information, see the "Granting access to the environment" section in [Provision Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span></span>

<span data-ttu-id="365e8-113">**วิธีแก้ปัญหาระยะยาว**</span><span class="sxs-lookup"><span data-stu-id="365e8-113">**Long-term solution**</span></span>

<span data-ttu-id="365e8-114">Microsoft กำลังพิจารณาการกำหนดสิทธิ์ที่เหมาะสมให้กับ Onboard และ Attract โดยอัตโนมัติ เมื่อผู้ใช้ถูกเพิ่มลงในทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="365e8-114">Microsoft is considering automatically assigning the appropriate rights to Onboard and Attract when a user is added to Human Resources.</span></span>
