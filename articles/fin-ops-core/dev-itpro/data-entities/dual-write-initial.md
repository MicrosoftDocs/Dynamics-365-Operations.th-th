---
title: ลำดับการดำเนินการสำหรับการซิงโครไนส์เริ่มต้นของแอพลิเคชัน Finance and Operations และ Common Data Service
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
ms.openlocfilehash: 3110cb809558d168e9d97f640701b249caf73f6c
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184519"
---
# <a name="execution-order-for-initial-synchronization-of-finance-and-operations-apps-and-common-data-service"></a><span data-ttu-id="def9e-103">ลำดับการดำเนินการสำหรับการซิงโครไนส์เริ่มต้นของแอพลิเคชัน Finance and Operations และ Common Data Service</span><span class="sxs-lookup"><span data-stu-id="def9e-103">Execution order for initial synchronization of Finance and Operations apps and Common Data Service</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

<span data-ttu-id="def9e-104">ก่อนที่คุณจะใช้การรวมข้อมูล คุณต้องสร้างข้อมูลเริ่มต้นที่จำเป็นสำหรับลูกค้า ผู้จัดจำหน่าย และผู้ติดต่อ</span><span class="sxs-lookup"><span data-stu-id="def9e-104">Before you use data integration, you must create the initial data that is required for customers, vendors, and contacts.</span></span> <span data-ttu-id="def9e-105">ตัวอย่างเช่น คุณต้องการสร้างสินค้าใน **กลุ่มผู้จัดจำหน่าย** ใหม่ และตั้งค่า **เงื่อนไขของการชำระเงิน** เป็น **Net30**</span><span class="sxs-lookup"><span data-stu-id="def9e-105">For example, you want to create a new **Vendor group** item and set its **Terms of Payment** value to **Net30**.</span></span> <span data-ttu-id="def9e-106">ในกรณีนี้ ก่อนที่คุณจะพยายามสร้างสินค้า **กลุ่มผู้จัดจำหน่าย**\* คุณต้องตรวจสอบให้แน่ใจว่า **Net30** มีอยู่ทั้งในแอพลิเคชันและ Common Data Service</span><span class="sxs-lookup"><span data-stu-id="def9e-106">In this case, before you try to create the **Vendor group** item, you must make sure that **Net30** exists in both the application and Common Data Service.</span></span> <span data-ttu-id="def9e-107">(ในอนาคต Microsoft จะนำออกใช้ฟังก์ชันแพลตฟอร์มการเขียนแบบคู่ที่เรียกว่า การซิงค์ครั้งแรก ฟังก์ชันนี้จะทำให้การซิงโครไนส์ข้อมูลแบบครั้งเดียวระหว่างแอพลิเคชันและ Common Data Service เป็นส่วนหนึ่งของการตั้งค่าการเขียนแบบคู่)</span><span class="sxs-lookup"><span data-stu-id="def9e-107">(In the future, Microsoft will release dual-write platform functionality that is named Initial Sync. This functionality will do a one-time data synchronization between the application and Common Data Service as part of the dual-write setup.)</span></span>

> [!TIP]
> <span data-ttu-id="def9e-108">Microsoft กำลังนำออกใช้แผนผังการเขียนแบบคู่สำหรับข้อมูลอ้างอิงทั้งหมด ซึ่งรวมถึง **เงื่อนไขของการชำระเงิน** (เงื่อนไขการชำระเงิน)</span><span class="sxs-lookup"><span data-stu-id="def9e-108">Microsoft is releasing a dual-write map for all reference data, including **Terms of Payment** (payment terms).</span></span> <span data-ttu-id="def9e-109">ถ้าคุณมีข้อมูลเริ่มต้นในระบบหนึ่งแล้ว การดำเนินการปรับปรุงขนาดเล็กบนเรกคอร์ดสามารถทริกเกอร์การเขียนแบบคู่บนเรกคอร์ดนั้นได้</span><span class="sxs-lookup"><span data-stu-id="def9e-109">If you already have the initial data in one system, a small update operation on a record can trigger dual-write on that record.</span></span>

<span data-ttu-id="def9e-110">คุณต้องทำตามลำดับของความสำคัญต่อไปนี้ และตรวจสอบให้แน่ใจว่าข้อมูลเริ่มต้นพร้อมใช้งานในทั้งแอพลิเคชัน และ Common Data Service</span><span class="sxs-lookup"><span data-stu-id="def9e-110">You must follow the following order of precedence and make sure that the initial data is available in the application and Common Data Service.</span></span>

## <a name="vendor"></a><span data-ttu-id="def9e-111">ผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="def9e-111">Vendor</span></span>

<span data-ttu-id="def9e-112">นี่คือลำดับของการดำเนินการสำหรับเอนทิตี้ **ผู้จัดจำหน่าย** :</span><span class="sxs-lookup"><span data-stu-id="def9e-112">Here is the order of execution for the **Vendor** entity:</span></span>

1. <span data-ttu-id="def9e-113">กลุ่มผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="def9e-113">Vendor group</span></span>

    1. <span data-ttu-id="def9e-114">เงื่อนไขการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="def9e-114">Terms of payment</span></span>

        1. <span data-ttu-id="def9e-115">วันที่ชำระเงินและรายการ</span><span class="sxs-lookup"><span data-stu-id="def9e-115">Payment day and lines</span></span>
        2. <span data-ttu-id="def9e-116">กำหนดการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="def9e-116">Payment schedule</span></span>

2. <span data-ttu-id="def9e-117">วิธีการชำระเงินของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="def9e-117">Vendor payment method</span></span>

## <a name="customer-organization"></a><span data-ttu-id="def9e-118">ลูกค้า (องค์กร)</span><span class="sxs-lookup"><span data-stu-id="def9e-118">Customer (Organization)</span></span>

<span data-ttu-id="def9e-119">นี่คือลำดับของการดำเนินการสำหรับเอนทิตี **ลูกค้า** :</span><span class="sxs-lookup"><span data-stu-id="def9e-119">Here is the order of execution for the **Customer** entity:</span></span>

1. <span data-ttu-id="def9e-120">กลุ่มลูกค้า</span><span class="sxs-lookup"><span data-stu-id="def9e-120">Customer group</span></span>

    1. <span data-ttu-id="def9e-121">เงื่อนไขการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="def9e-121">Terms of payment</span></span>

        1. <span data-ttu-id="def9e-122">วันที่ชำระเงินและรายการ</span><span class="sxs-lookup"><span data-stu-id="def9e-122">Payment day and lines</span></span>
        2. <span data-ttu-id="def9e-123">การชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="def9e-123">Payment</span></span> 

2. <span data-ttu-id="def9e-124">วิธีการชำระเงินของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="def9e-124">Customer payment method</span></span>

## <a name="contact-person"></a><span data-ttu-id="def9e-125">ผู้ติดต่อ (บุคคล)</span><span class="sxs-lookup"><span data-stu-id="def9e-125">Contact (Person)</span></span>

<span data-ttu-id="def9e-126">นี่คือลำดับของการดำเนินการสำหรับเอนทิตี **ผู้ติดต่อ** :</span><span class="sxs-lookup"><span data-stu-id="def9e-126">Here is the order of execution for the **Contact** entity:</span></span>

1. <span data-ttu-id="def9e-127">ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="def9e-127">Customer</span></span>
2. <span data-ttu-id="def9e-128">ผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="def9e-128">Vendor</span></span>
