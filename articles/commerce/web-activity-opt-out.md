---
title: การเลือกปฏิเสธการรวบรวมข้อมูลกิจกรรมบนเว็บ
description: หัวข้อนี้อธิบายถึงวิธีการที่คุณสามารถอนุญาตให้ผู้เยี่ยมชมเว็บไซต์ของคุณเลือกใช้งานการรวบรวมข้อมูลกิจกรรมบนเว็บใน Microsoft Dynamics 365 Commerce
author: aamiral
manager: AnnBe
ms.date: 05/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 244d612fa01529df4fff250df50a06526632fcf1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5210934"
---
# <a name="opt-out-of-web-activity-event-collection"></a><span data-ttu-id="68f75-103">การเลือกปฏิเสธการรวบรวมข้อมูลกิจกรรมบนเว็บ</span><span class="sxs-lookup"><span data-stu-id="68f75-103">Opt out of web activity event collection</span></span>
[!include [banner](includes/banner.md)]

<span data-ttu-id="68f75-104">หัวข้อนี้อธิบายวิธีที่คุณสามารถให้ลูกค้าเลือกที่จะไม่รับการรวบรวมข้อมูลกิจกรรมบนเว็บใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="68f75-104">This topic explains how you can let customers opt out of web activity event collection in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="68f75-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="68f75-105">Overview</span></span>

<span data-ttu-id="68f75-106">Dynamics 365 Commerce ช่วยให้ผู้ดูแลไซต์วิเคราะห์กิจกรรมบนเว็บของผู้ใช้เว็บไซต์อีคอมเมิร์ซของตน</span><span class="sxs-lookup"><span data-stu-id="68f75-106">Dynamics 365 Commerce lets site administrators analyze the web activity of users of their e-commerce sites.</span></span> <span data-ttu-id="68f75-107">วิธีการนี้จะทำให้ผู้ใช้สามารถเข้าใจวิธีการใช้ไซต์ของตนได้ดียิ่งขึ้นและสามารถเพิ่มประสิทธิภาพให้กับไซต์เพื่อให้ประสบการณ์การใช้งานของผู้ใช้ที่ดีขึ้นและเป็นไปตามวัตถุประสงค์ทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="68f75-107">In that way, they can better understand how their sites are used, and they can optimize the sites to provide an improved user experience and meet business objectives.</span></span>


## <a name="ways-for-administrators-to-implement-an-opt-out-experience"></a><span data-ttu-id="68f75-108">วิธีที่ผู้ดูแลระบบจะใช้ประสบการณ์การปฏิเสธเข้าร่วม</span><span class="sxs-lookup"><span data-stu-id="68f75-108">Ways for administrators to implement an opt-out experience</span></span>

<span data-ttu-id="68f75-109">ผู้ดูแลระบบมีสามวิธีที่จะใช้ประสบการณ์การปฏิเสธเข้าร่วม</span><span class="sxs-lookup"><span data-stu-id="68f75-109">Administrators have three ways to implement an opt-out experience.</span></span>

### <a name="opt-out-on-behalf-of-users"></a><span data-ttu-id="68f75-110">ปฏิเสธเข้าร่วมที่กระทำในนามของผู้ใช้อื่น</span><span class="sxs-lookup"><span data-stu-id="68f75-110">Opt out on behalf of users</span></span>

<span data-ttu-id="68f75-111">ในการจัดการลูกค้าองค์กรในศูนย์ควบคุม Commerce ผู้ดูแลระบบสามารถปฏิเสธเข้าร่วมในนามของผู้ใช้อื่น</span><span class="sxs-lookup"><span data-stu-id="68f75-111">In Account management in Commerce headquarters (HQ), administrators can opt out on behalf of users.</span></span>

1. <span data-ttu-id="68f75-112">ในไคลเอนต์ HQ บนหน้า **ลูกค้าทั้งหมด** ให้ค้นหาและเลือกลูกค้า</span><span class="sxs-lookup"><span data-stu-id="68f75-112">In the HQ client, on the **All customers** page, search for and select a customer.</span></span>
1. <span data-ttu-id="68f75-113">บนหน้ารายละเอียดลูกค้าบนแท็บด่วน **การขายปลีก** ในส่วน **ความเป็นส่วนตัว** ให้ตั้งค่าตัวเลือก **อย่าติดตามกิจกรรมของเว็บ** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="68f75-113">On the customer details page, on the **Retail** FastTab, in the **Privacy** section, set the **Do not track web activity** option to **Yes**.</span></span>

    ![การตั้งค่าความเป็นส่วนตัว](media/Disablepersonalizationpart2.png)

1. <span data-ttu-id="68f75-115">เลือก **ตกลง** และจากนั้นปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="68f75-115">Select **Save**, and then close the page.</span></span>

### <a name="module-based-opt-out-experience"></a><span data-ttu-id="68f75-116">ประสบการณ์การเลือกไม่ใช้การยึดตามโมดูล</span><span class="sxs-lookup"><span data-stu-id="68f75-116">Module-based opt-out experience</span></span>

<span data-ttu-id="68f75-117">ผู้ดูแลระบบสามารถอนุญาตให้ผู้ใช้ที่ได้รับการรับรองความถูกต้องเลือกที่จะไม่ใช้งานการรวบรวมข้อมูลกิจกรรมบนเว็บด้วยตัวเอง</span><span class="sxs-lookup"><span data-stu-id="68f75-117">Administrators can let authenticated users opt out of web activity event collection by themselves.</span></span> <span data-ttu-id="68f75-118">เพื่อมอบประสบการณ์การไม่เข้าร่วมนี้ ให้เพิ่มโมดูลการยกเลิกผู้ใช้ในหน้าโปรไฟล์บัญชีลูกค้า</span><span class="sxs-lookup"><span data-stu-id="68f75-118">To provide this opt-out experience, add the user opt-out module to customer account profile pages.</span></span>

### <a name="custom-extensions"></a><span data-ttu-id="68f75-119">ส่วนขยายที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="68f75-119">Custom extensions</span></span>

<span data-ttu-id="68f75-120">ผู้ดูแลระบบสามารถสร้างส่วนขยายของตนเองเพื่อจัดการประสบการณ์การเลือกไม่ใช้สำหรับผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="68f75-120">Administrators can create their own extensions to manage the opt-out experience for users.</span></span> <span data-ttu-id="68f75-121">สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [เรียกเซิร์ฟเวอร์การขายปลีก API](e-commerce-extensibility/call-retail-server-apis.md) และ [การเพิ่มช่องทางออนไลน์](e-commerce-extensibility/overview.md)</span><span class="sxs-lookup"><span data-stu-id="68f75-121">For more information, see [Call Retail Server APIs](e-commerce-extensibility/call-retail-server-apis.md) and [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]