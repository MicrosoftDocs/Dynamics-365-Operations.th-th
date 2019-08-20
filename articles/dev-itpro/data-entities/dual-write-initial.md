---
title: ลำดับการดำเนินการสำหรับการซิงโครไนส์เริ่มต้นของ Finance and Operations และ Common Data Service
description: หัวข้อนี้ระบุลำดับของการซิงโครไนส์ที่คุณต้องปฏิบัติตามเพื่อสร้างข้อมูลเริ่มต้น
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: b74bc2d3133af7e87663a4e6bafb8780e0a6a66f
ms.sourcegitcommit: efcc0dee8bde5f8f93f6291e7f059ad426843e57
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 07/31/2019
ms.locfileid: "1797309"
---
# <a name="execution-order-for-initial-sychronization-of-finance-and-operations-and-common-data-service"></a><span data-ttu-id="9c474-103">ลำดับการดำเนินการสำหรับการซิงโครไนส์เริ่มต้นของ Finance and Operations และ Common Data Service</span><span class="sxs-lookup"><span data-stu-id="9c474-103">Execution order for initial sychronization of Finance and Operations and Common Data Service</span></span>

<span data-ttu-id="9c474-104">ก่อนที่คุณจะใช้การรวมข้อมูล คุณต้องสร้างข้อมูลเริ่มต้นที่จำเป็นสำหรับลูกค้า ผู้จัดจำหน่าย และผู้ติดต่อ</span><span class="sxs-lookup"><span data-stu-id="9c474-104">Before you use data integration, you must create the initial data required for customers, vendors and contacts.</span></span> <span data-ttu-id="9c474-105">ตัวอย่างเช่น ถ้าคุณต้องการสร้างรายการของ **กลุ่มผู้จัดจำหน่าย** ใหม่ และตั้งค่า **เงื่อนไขของการชำระเงิน** เป็น **Net30** จากนั้น ก่อนที่คุณจะพยายามสร้างรายการ **กลุ่มผู้จัดจำหน่าย** คุณต้องตรวจสอบให้แน่ใจว่า **Net30** พร้อมใช้งานในทั้ง Finance and Operations และ Common Data Service</span><span class="sxs-lookup"><span data-stu-id="9c474-105">For example, if you want to create a new **Vendor group** item and set its **Terms of Payment** as **Net30**, then before you attempt to create the **Vendor group** item you need to make sure that **Net30** exists in both Finance and Operations and Common Data Service.</span></span> <span data-ttu-id="9c474-106">(ในอนาคต เราจะนำออกใช้ฟังก์ชันแพลตฟอร์มการเขียนแบบคู่ที่เรียกว่า **การซิงค์ครั้งแรก** จะทำให้การซิงโครไนส์ข้อมูลแบบครั้งเดียวระหว่าง Finance and Operations และ Common Data Service เป็นส่วนหนึ่งของการตั้งค่าการเขียนแบบคู่)</span><span class="sxs-lookup"><span data-stu-id="9c474-106">(In the future, we will release a  dual-write platform functionality called **Initial Sync**. It will do a one-time data synchronization between Finance and Operations and Common Data Service as part of the dual-write setup.)</span></span>

<span data-ttu-id="9c474-107">เคล็ดลับ: เรากำลังนำออกใช้แผนผังการเขียนแบบคู่สำหรับข้อมูลอ้างอิงทั้งหมด ซึ่งรวมถึง **เงื่อนไขของการชำระเงิน** (เงื่อนไขการชำระเงิน)</span><span class="sxs-lookup"><span data-stu-id="9c474-107">Tips: We are releasing a dual-write map for all reference data including **Terms of Payment** (Payment Terms).</span></span> <span data-ttu-id="9c474-108">ถ้าคุณมีข้อมูลเริ่มต้นในระบบหนึ่งแล้ว การดำเนินการปรับปรุงขนาดเล็กบนเรกคอร์ดสามารถทริกเกอร์การเขียนแบบคู่บนเรกคอร์ดนั้นได้</span><span class="sxs-lookup"><span data-stu-id="9c474-108">If you already have the initial data in one system, a small update operation on a record can trigger dual-write on that record.</span></span> 

<span data-ttu-id="9c474-109">คุณต้องทำตามลำดับความสำคัญต่อไปนี้และตรวจสอบให้แน่ใจว่าข้อมูลเริ่มต้นพร้อมใช้งานในทั้ง Finance and Operations และ Common Data Service</span><span class="sxs-lookup"><span data-stu-id="9c474-109">You must follow the following order of precedence and make sure that the initial data is available on both Finance and Operations and Common Data Service.</span></span>   

## <a name="vendor"></a><span data-ttu-id="9c474-110">ผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="9c474-110">Vendor</span></span>

<span data-ttu-id="9c474-111">ลำดับของการดำเนินการสำหรับผู้จัดจำหน่ายคือ:</span><span class="sxs-lookup"><span data-stu-id="9c474-111">The order of execution for Vendor is:</span></span>

```
Vendor Group
    Terms of payment
        Payment day & lines
        Payment schedule
Vendor payment method
```

## <a name="customer-organization"></a><span data-ttu-id="9c474-112">ลูกค้า (องค์กร)</span><span class="sxs-lookup"><span data-stu-id="9c474-112">Customer (Organization)</span></span>

<span data-ttu-id="9c474-113">ลำดับของการดำเนินการสำหรับลูกค้าคือ:</span><span class="sxs-lookup"><span data-stu-id="9c474-113">The order of execution for Customer is:</span></span>

```
Customer Group
    Terms of payment
        Payment day & lines
        Payment 
Customer payment method
```

## <a name="contact-person"></a><span data-ttu-id="9c474-114">ผู้ติดต่อ (บุคคล)</span><span class="sxs-lookup"><span data-stu-id="9c474-114">Contact (Person)</span></span>

<span data-ttu-id="9c474-115">ลำดับของการดำเนินการสำหรับผู้ติดต่อคือ:</span><span class="sxs-lookup"><span data-stu-id="9c474-115">The order of execution for Contact is:</span></span>

```
Customer
Vendor               
```
