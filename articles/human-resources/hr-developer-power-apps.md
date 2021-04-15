---
title: ขยาย Talent ด้วย Power Apps และ Power Automate
description: บทความนี้อธิบายถึงตัวอย่างบางอย่างของสถานการณ์สมมุติของการเพิ่มความสามารถของ Microsoft Dynamics 365 Human Resources ที่ใช้ Microsoft Power Apps และ Microsoft Power Automate
author: negudava
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ad55de4b660de89d323f32a1ce2911d880c24ec5
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5793572"
---
# <a name="extend-with-power-apps-and-power-automate"></a><span data-ttu-id="10abc-103">ขยายด้วย Power Apps และ Power Automate</span><span class="sxs-lookup"><span data-stu-id="10abc-103">Extend with Power Apps and Power Automate</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="10abc-104">บทความนี้อธิบายถึงตัวอย่างบางอย่างของสถานการณ์สมมุติของการเพิ่มความสามารถของ Microsoft Dynamics 365 Human Resources ที่ใช้ Microsoft Power Apps และ Microsoft Power Automate</span><span class="sxs-lookup"><span data-stu-id="10abc-104">This article describes some examples of extensibility scenarios for Microsoft Dynamics 365 Human Resources that use Microsoft Power Apps and Microsoft Power Automate.</span></span> <span data-ttu-id="10abc-105">คุณสามารถนำเข้าโซลูชันแพคเกจที่เชื่อมโยงกับแต่ละตัวอย่างไปยังสภาพแวดล้อม Power Apps ของคุณ</span><span class="sxs-lookup"><span data-stu-id="10abc-105">You can import the solution package that is associated with each example into your Power Apps environment.</span></span> <span data-ttu-id="10abc-106">จากนั้นคุณสามารถใช้แพคเกจเป็นคำแนะนำหรือเป็นจุดเริ่มต้นเพื่อนำสถานการณ์ที่สามารถใช้ได้กับองค์กรของคุณไปใช้</span><span class="sxs-lookup"><span data-stu-id="10abc-106">You can then use the packages either as guidance or as starting points to implement scenarios that are applicable to your organization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="10abc-107">ถ้าคุณต้องการใช้แม่แบบและแอปที่อธิบายไว้ในหัวข้อนี้ "ตามที่เป็น" ให้แน่ใจว่าได้ทดสอบแล้วเพื่อให้แน่ใจว่าจะครอบคลุมสถานการณ์ทั้งหมดที่เกี่ยวข้องกับการนำไปใช้ของคุณโดยเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="10abc-107">If you want to use the templates and apps that are described in this topic "as is," be sure to test them to make sure that they cover all the scenarios that are specific to your implementation.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="10abc-108">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="10abc-108">Prerequisites</span></span>

- <span data-ttu-id="10abc-109">เมื่อต้องการนำเข้าแพคเกจ ผู้ใช้ต้องมีสิทธิ์ **ผู้สร้างสภาพแวดล้อม**</span><span class="sxs-lookup"><span data-stu-id="10abc-109">To import packages, users must have the **Environment Maker** permission.</span></span>
- <span data-ttu-id="10abc-110">เมื่อต้องการส่งออกหรือนำเข้าแอป ผู้ใช้ต้องมีใบอนุญาตใช้ Power Apps Plan 2 หรือใบอนุญาตในการทดลองใช้ Power Apps Plan 2</span><span class="sxs-lookup"><span data-stu-id="10abc-110">To export or import apps, users must have a Power Apps Plan 2 license or a Power Apps Plan 2 trial license.</span></span>

## <a name="integration-with-microsoft-365-power-automate"></a><span data-ttu-id="10abc-111">การรวมกับ Microsoft 365, Power Automate</span><span class="sxs-lookup"><span data-stu-id="10abc-111">Integration with Microsoft 365, Power Automate</span></span>

<span data-ttu-id="10abc-112">คุณสามารถใช้แอป **การรวมกับ Microsoft 365** ในการดึงข้อมูลของทีมงานสำหรับผู้ใช้ที่ลงชื่อเข้าใช้จาก Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="10abc-112">The **Integration with Microsoft 365** app can be used to extract team information for signed-in users from Microsoft 365.</span></span> <span data-ttu-id="10abc-113">อ้างอิงผู้ปฏิบัติงานในทรัพยากรบุคคลเพื่อแยกชนิดหมายเลขประจำตัวของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="10abc-113">It references workers in Human Resources to extract employee identification types.</span></span> <span data-ttu-id="10abc-114">ผู้จัดการสามารถตรวจสอบวันหมดอายุของชนิดรหัสพนักงาน</span><span class="sxs-lookup"><span data-stu-id="10abc-114">Managers can check expiration dates of employee ID types.</span></span> <span data-ttu-id="10abc-115">นอกจากนี้คุณยังสามารถส่งตัวเตือนทางอีเมลได้ถ้าชนิดรหัสพนักงานหมดอายุ</span><span class="sxs-lookup"><span data-stu-id="10abc-115">They can also send an email reminder if the employee ID type is expiring.</span></span> <span data-ttu-id="10abc-116">Power Automate รวมกับ Power Apps เพื่อส่งจดหมายเตือนนี้</span><span class="sxs-lookup"><span data-stu-id="10abc-116">Power Automate integrates with Power Apps to send this reminder.</span></span> <span data-ttu-id="10abc-117">การยืนยันจะถูกส่งกลับไป Power Apps จาก Power Automate เมื่อการเตือนถูกส่งออกไป</span><span class="sxs-lookup"><span data-stu-id="10abc-117">Confirmation will be sent back to Power Apps from Power Automate when the reminder is sent.</span></span> <span data-ttu-id="10abc-118">ชนิดของการระบุรหัสประจำตัว รวมถึงใบอนุญาตของพนักงานขนส่ง พาสปอร์ต และแบบฟอร์มที่ยอมรับได้อื่นๆของผู้ขับขี่</span><span class="sxs-lookup"><span data-stu-id="10abc-118">Identification types include driver's license, passport, and other acceptable forms of ID.</span></span>

<span data-ttu-id="10abc-119">คุณสามารถขยายแอปสำหรับสถานการณ์อื่นๆ</span><span class="sxs-lookup"><span data-stu-id="10abc-119">You can extend this app for other scenarios.</span></span> <span data-ttu-id="10abc-120">ตัวอย่างเช่น คุณสามารถใช้เพื่อแสดงข้อมูลวันหยุดพักผ่อนของทีมงาน ปฏิทินเหตุการณ์ และเหตุการณ์เฉพาะทีมงานใด ๆ</span><span class="sxs-lookup"><span data-stu-id="10abc-120">For example, you can use it to show team vacation information, calendar events, and any team-specific events.</span></span>

<span data-ttu-id="10abc-121">เมื่อต้องการดาวน์โหลดแอป **การรวมกับ Microsoft 365, Power Automate** ให้ไปที่ [การรวมกับ Microsoft 365](https://go.microsoft.com/fwlink/?linkid=2081787) บนศูนย์ดาวน์โหลด Microsoft</span><span class="sxs-lookup"><span data-stu-id="10abc-121">To download the **Integration with Microsoft 365, Power Automate** app, go to [Integration with Microsoft 365](https://go.microsoft.com/fwlink/?linkid=2081787) on the Microsoft Download Center.</span></span>

## <a name="power-automate--sql-connect-and-execute"></a><span data-ttu-id="10abc-122">Power Automate – การเชื่อมต่อและดำเนินการ SQL</span><span class="sxs-lookup"><span data-stu-id="10abc-122">Power Automate – SQL Connect and execute</span></span>

<span data-ttu-id="10abc-123">แม่แบบ **Power Automate – การเชื่อมต่อและดำเนินการ SQL** เชื่อมต่อกับ Microsoft SQL Server และเปิดใช้งานให้การสอบถาม SQL รัน</span><span class="sxs-lookup"><span data-stu-id="10abc-123">The **Power Automate – SQL Connect and execute** template connects to Microsoft SQL Server and enables SQL queries to be run.</span></span>

<span data-ttu-id="10abc-124">ถึงแม้ว่าแม่แบบนี้จะอ่านและอัปเดตตาราง SQL คุณสามารถขยายและใช้งานสำหรับสถานการณ์อื่นๆได้</span><span class="sxs-lookup"><span data-stu-id="10abc-124">Although this template reads and updates SQL tables, you can extend it and use it for other scenarios.</span></span> <span data-ttu-id="10abc-125">ตัวอย่างเช่น คุณสามารถใช้เพื่อกรอกข้อมูลในตารางการจัดเตรียมใน Dataverse ด้วยเรกคอร์ดจากเซิร์ฟเวอร์ SQL และเพื่อซิงโครไนส์ตารางการจัดเตรียมเป็นระยะ ๆ โดยใช้พุชส่วนเพิ่มจากเซิร์ฟเวอร์ SQL </span><span class="sxs-lookup"><span data-stu-id="10abc-125">For example, you can use it to fill a staging table in Dataverse with records from SQL Server, and to periodically synchronize the staging table by using an incremental push from SQL Server.</span></span>

<span data-ttu-id="10abc-126">การสอบถามขั้นสูงถูกรวมเข้ากับขั้นตอนในการเปิดใช้งานการแปลงข้อมูลและการผลักข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="10abc-126">Advanced Query is integrated with Flow to enable Data transformation and incremental push.</span></span>

<span data-ttu-id="10abc-127">เมื่อต้องการดาวน์โหลดแม่แบบ **Power Automate – การเชื่อมต่อและดำเนินการ SQL** ไปที่ [Power Automate – การเชื่อมต่อและดำเนินการ SQL](https://go.microsoft.com/fwlink/?linkid=2081789) บนศูนย์ดาวน์โหลด Microsoft</span><span class="sxs-lookup"><span data-stu-id="10abc-127">To download the **Power Automate – SQL Connect and execute** template, go to [Power Automate – SQL Connect and execute](https://go.microsoft.com/fwlink/?linkid=2081789) on the Microsoft Download Center.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="10abc-128">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="10abc-128">Additional resources</span></span>

[<span data-ttu-id="10abc-129">Microsoft Power Platform</span><span class="sxs-lookup"><span data-stu-id="10abc-129">The Microsoft Power Platform</span></span>](https://docs.microsoft.com/power-platform/admin/admin-documentation)</br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]