---
title: เปิดใช้งานการรวม Broadbean ใน Attract
description: หัวข้อนี้อธิบายถึงวิธีการตั้งค่าคอนฟิก Microsoft Dynamics 365 Talent - Attract เพื่อลงรายการบัญชีงานไปยังบอร์ดงานภายนอก เช่น Broadbean
author: andreabichsel
manager: AnnBe
ms.date: 07/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-07-08
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 10b612711e81b2b368ed23fdd95ab6a66451f0ca
ms.sourcegitcommit: 9cc6a011bfdd1b0fe505760b6bf429eb6c65862a
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/25/2019
ms.locfileid: "2833219"
---
# <a name="enable-broadbean-integration-in-attract"></a><span data-ttu-id="dfdf3-103">เปิดใช้งานการรวม Broadbean ใน Attract</span><span class="sxs-lookup"><span data-stu-id="dfdf3-103">Enable Broadbean integration in Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="dfdf3-104">คุณต้องการเรียกดูตำแหน่งที่เปิดของคุณ ข้างหน้าผู้สมัครที่มีคุณสมบัติหลายรายที่สุดที่เป็นไปได้</span><span class="sxs-lookup"><span data-stu-id="dfdf3-104">You want to get your open positions in front of as many qualified candidates as possible.</span></span> <span data-ttu-id="dfdf3-105">ไซต์การสรรหาบุคลากร เช่น Broadbean ช่วยให้คุณบรรลุถึงเป้าหมายนี้</span><span class="sxs-lookup"><span data-stu-id="dfdf3-105">Recruiting sites such as Broadbean help you accomplish this goal.</span></span> <span data-ttu-id="dfdf3-106">Microsoft Dynamics 365 Talent: Attract: ตอนนี้สามารถช่วยให้คุณลงประกาศงานไปยัง Broadbean ได้แล้ว และ Microsoft ได้ให้ข้อเสนอใหม่ในพื้นที่นี้ตลอดเวลา</span><span class="sxs-lookup"><span data-stu-id="dfdf3-106">Microsoft Dynamics 365 Talent: Attract now lets you post jobs to Broadbean, and Microsoft is constantly providing new offerings in this area.</span></span>

> [!NOTE]
> - <span data-ttu-id="dfdf3-107">เพื่อลงประกาศงานไปยังไซต์ภายนอก คุณต้องมี [add-on การว่าจ้างที่ครอบคลุม](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring)</span><span class="sxs-lookup"><span data-stu-id="dfdf3-107">To post jobs to external sites, you must have the [Comprehensive hiring add-on](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).</span></span>
> - <span data-ttu-id="dfdf3-108">เมื่อต้องการลงรายการบัญชีงานไปยัง Broadbean ผ่าน Attract คุณต้องมีการสมัครใช้งาน Broadbean</span><span class="sxs-lookup"><span data-stu-id="dfdf3-108">To post jobs to Broadbean through Attract, you must have a Broadbean subscription.</span></span>
> - <span data-ttu-id="dfdf3-109">คุณลักษณะนี้อยู่ในการแสดงตัวอย่างในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="dfdf3-109">This feature is currently in preview.</span></span> <span data-ttu-id="dfdf3-110">ถ้าคุณต้องการลอง คุณต้อง [เปิดในการตั้งค่าการจัดการ Attract](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature)</span><span class="sxs-lookup"><span data-stu-id="dfdf3-110">If you want to try it, you must [turn it on in the Attract admin settings](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).</span></span>

## <a name="configure-broadbean-integration"></a><span data-ttu-id="dfdf3-111">ตั้งค่าคอนฟิกการรวม Broadbean</span><span class="sxs-lookup"><span data-stu-id="dfdf3-111">Configure Broadbean integration</span></span>

1. <span data-ttu-id="dfdf3-112">ลงชื่อเข้าใช้ Attract เป็นผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="dfdf3-112">Sign in to Attract as an admin.</span></span>

2. <span data-ttu-id="dfdf3-113">เลือกปุ่ม **การตั้งค่า** (สัญลักษณ์เกียร์) ในมุมขวาบนของหน้า และจากนั้น **ศูนย์การจัดการ**</span><span class="sxs-lookup"><span data-stu-id="dfdf3-113">Select the **Settings** button (the gear symbol) in the upper-right corner of the page, and then select **Admin center**.</span></span>

3. <span data-ttu-id="dfdf3-114">ติดต่อ Broadbean และป้อนข้อมูลของคุณใน **ชื่อผู้ใช้** **รหัสไคลเอนต์** และฟิลด์ **โทเคนการเข้ารหัส**</span><span class="sxs-lookup"><span data-stu-id="dfdf3-114">Contact Broadbean, and enter your information in the **Username**, **Client ID**, and **Encryption Token** fields.</span></span>

4. <span data-ttu-id="dfdf3-115">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="dfdf3-115">Select **Save**.</span></span>

> [!WARNING]
> <span data-ttu-id="dfdf3-116">ข้อมูลประจำตัว Broadbean ของคุณมีความสำคัญ และเป็นความลับ</span><span class="sxs-lookup"><span data-stu-id="dfdf3-116">Your Broadbean credentials are sensitive and confidential.</span></span> <span data-ttu-id="dfdf3-117">ดังนั้น จึงจัดเก็บ และแบ่งปันอย่างรับผิดชอบ</span><span class="sxs-lookup"><span data-stu-id="dfdf3-117">Therefore, store and share them responsibly.</span></span> <span data-ttu-id="dfdf3-118">ผู้ที่มีบทบาทผู้ดูแลระบบใน Attract สามารถดูข้อมูลประจำตัวเหล่านี้ได้</span><span class="sxs-lookup"><span data-stu-id="dfdf3-118">Anyone who has an Administrator role in Attract can view these credentials.</span></span>

> [!NOTE]
> <span data-ttu-id="dfdf3-119">Microsoft และ Attract จะไม่เกี่ยวข้องในการสร้างและการรักษาค่าเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="dfdf3-119">Microsoft and Attract aren't involved in creating and maintaining these values.</span></span> <span data-ttu-id="dfdf3-120">เป็นความรับผิดชอบของคุณในการทำให้เป็นปัจจุบันใน Attract และในการทำงานกับ Broadbean เพื่อแก้ไขปัญหาใดๆ ที่เกี่ยวข้องกับข้อมูลประจำตัวของคุณ</span><span class="sxs-lookup"><span data-stu-id="dfdf3-120">It's your responsibility to keep them up to date in Attract and to work with Broadbean to resolve any issues that involve your credentials.</span></span>
