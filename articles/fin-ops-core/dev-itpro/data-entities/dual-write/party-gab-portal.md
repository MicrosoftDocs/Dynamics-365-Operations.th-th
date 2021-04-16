---
title: การใช้ Power Portal กับรูปแบบข้อมูลฝ่าย
description: หัวข้อนี้จะอธิบายการเปลี่ยนแปลงไปยังบทบาทเว็บของ Power Portal เนื่องจากรูปแบบข้อมูลฝ่ายในการรวมแบบสองทิศทาง
author: RamaKrishnamoorthy
ms.date: 03/22/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-22
ms.openlocfilehash: a2ea914344341ee26138e853727c551bdd5d733e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833101"
---
# <a name="using-power-portal-with-the-party-data-model"></a><span data-ttu-id="35920-103">การใช้ Power Portal กับรูปแบบข้อมูลฝ่าย</span><span class="sxs-lookup"><span data-stu-id="35920-103">Using Power Portal with the Party data model</span></span>

[!INCLUDE[banner](../../includes/banner.md)]

[!INCLUDE[rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="35920-104">รุ่นโซลูชันการประสานกันของแอปพลิเคชันการรวมแบบสองทิศทาง 2.0.999.0 และรุ่นที่ใหม่กว่า รวมถึงการเปลี่ยนแปลงรูปแบบข้อมูลไปยังฝ่ายและสมุดที่อยู่สากลสำหรับตารางบัญชีและผู้ติดต่อ</span><span class="sxs-lookup"><span data-stu-id="35920-104">The Dual-write application orchestration solution version 2.0.999.0 and later includes data model changes to party and global address book for the Account and Contact tables.</span></span> <span data-ttu-id="35920-105">การเปลี่ยนแปลงอนุญาตให้มีความสัมพันธ์แบบกลุ่มต่อกลุ่มที่สนับสนุนสถานการณ์ทางธุรกิจขั้นสูง</span><span class="sxs-lookup"><span data-stu-id="35920-105">The changes allow many-to-many relationships that support advanced business scenarios.</span></span> <span data-ttu-id="35920-106">บทบาทเว็บพอร์ทัลไม่สนับสนุนการเปลี่ยนแปลงเหล่านี้ ซึ่งรวมถึงพอร์ทัลของลูกค้า ที่มีการจัดส่งแบบสำเร็จรูปหรือที่มีอยู่ในสภาพแวดล้อมของคุณ ก่อนที่คุณจะติดตั้งการรวมแบบสองทิศทาง</span><span class="sxs-lookup"><span data-stu-id="35920-106">These changes are not supported by portal web roles, including the customer portal, that are shipped out-of-the-box or that existed in your environment before you installed dual-write.</span></span> <span data-ttu-id="35920-107">เพื่อให้บทบาทเว็บทำงานตามที่คาดไว้ คุณต้องสร้างบทบาทเว็บใหม่โดยใช้รูปแบบข้อมูลใหม่</span><span class="sxs-lookup"><span data-stu-id="35920-107">For the web roles to work as expected, you need to create new web roles using the new data model.</span></span> 

<span data-ttu-id="35920-108">โดยสรุป วิธีที่ตารางโต้ตอบมีการเปลี่ยนแปลง แต่สิทธิ์ของตารางในพอร์ทัลลูกค้ายังไม่ได้เปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="35920-108">In summary, the way the tables interact has changed, but the table permissions in the customer portal haven't changed.</span></span> <span data-ttu-id="35920-109">หัวข้อนี้อธิบายวิธีการสร้างบทบาทเว็บใหม่ที่ทำงานกับรูปแบบข้อมูลขั้นสูงใหม่</span><span class="sxs-lookup"><span data-stu-id="35920-109">This topic explains how to create new web roles that work with the new advanced data model.</span></span>

<span data-ttu-id="35920-110">แผนภาพนี้แสดงความสัมพันธ์ของตาราง **ที่ไม่มี** ฝ่ายและรูปแบบข้อมูลสมุดที่อยู่สากล:</span><span class="sxs-lookup"><span data-stu-id="35920-110">This diagram shows the table relationship **without** the party and global address book data model:</span></span>

   ![โดยไม่มีแบบจำลองฝ่าย](media/without-party-model.PNG)

<span data-ttu-id="35920-112">แผนภาพนี้แสดงความสัมพันธ์ของตาราง **ที่มี** ฝ่ายและรูปแบบข้อมูลสมุดที่อยู่สากล:</span><span class="sxs-lookup"><span data-stu-id="35920-112">This diagram shows the table relationship **with** the party and global address book data model:</span></span>

   ![โดยมีแบบจำลองฝ่าย](media/with-party-model.png)

## <a name="create-a-new-table-permission"></a><span data-ttu-id="35920-114">สร้างสิทธิ์ของตารางใหม่</span><span class="sxs-lookup"><span data-stu-id="35920-114">Create a new table permission</span></span>

<span data-ttu-id="35920-115">หากต้องการสร้างสิทธิ์ของตารางใหม่เหล่านี้ ให้ปฏิบัติตามขั้นตอนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="35920-115">To create these new table permissions, follow these steps:</span></span>

1. <span data-ttu-id="35920-116">ลงชื่อเข้าใช้ [Power Apps](https://make.powerapps.com) และไปที่แอปของคุณ</span><span class="sxs-lookup"><span data-stu-id="35920-116">Sign in to [Power Apps](https://make.powerapps.com), and go to your apps.</span></span>
2. <span data-ttu-id="35920-117">เลือกแอปการจัดการพอร์ทัลของคุณ</span><span class="sxs-lookup"><span data-stu-id="35920-117">Select your Portal Management app.</span></span>
3. <span data-ttu-id="35920-118">ในแถบด้านข้าง ให้เลือก **ความปลอดภัย > สิทธิ์ของตาราง**</span><span class="sxs-lookup"><span data-stu-id="35920-118">In the side bar, select **Security > Table permissions**.</span></span>

    <span data-ttu-id="35920-119">คุณต้องสร้างสิทธิ์ใหม่สามสิทธิ์:</span><span class="sxs-lookup"><span data-stu-id="35920-119">You must create three new permissions:</span></span>

    + <span data-ttu-id="35920-120">การเชื่อมต่อของผู้ติดต่อไปยังฝ่าย</span><span class="sxs-lookup"><span data-stu-id="35920-120">Contact to Party connection</span></span>
    + <span data-ttu-id="35920-121">การเชื่อมต่อของฝ่ายไปยังบัญชี</span><span class="sxs-lookup"><span data-stu-id="35920-121">Party to Account connection</span></span>
    + <span data-ttu-id="35920-122">การเชื่อมต่อของบัญชีไปยังใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="35920-122">Account to Order connection</span></span>

4. <span data-ttu-id="35920-123">สร้างและบันทึกสิทธิ์ใหม่สำหรับการเชื่อมต่อของผู้ติดต่อไปยังฝ่าย โดยตั้งค่าพารามิเตอร์เหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="35920-123">Create and save a new permission for the Contact to Party connection, setting these parameters:</span></span>

    + <span data-ttu-id="35920-124">**ชื่อ**: การเชื่อมต่อของฝ่ายไปยังบัญชี (หรือที่คุณเลือก)</span><span class="sxs-lookup"><span data-stu-id="35920-124">**Name**: Party to Account Connection (or your choice)</span></span>
    + <span data-ttu-id="35920-125">**ชื่อตาราง**: msdyn_contactforparty</span><span class="sxs-lookup"><span data-stu-id="35920-125">**Table Name**: msdyn_contactforparty</span></span>
    + <span data-ttu-id="35920-126">**เว็บไซต์**: พอร์ทัลของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="35920-126">**Website**: Customer Portal</span></span>
    + <span data-ttu-id="35920-127">**ขอบเขต**: ผู้ติดต่อ</span><span class="sxs-lookup"><span data-stu-id="35920-127">**Scope**: Contact</span></span>
    + <span data-ttu-id="35920-128">**สิทธิ์**: เลือกทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="35920-128">**Privileges**: Select all</span></span>
    + <span data-ttu-id="35920-129">**บทบาทเว็บ**: ผู้ใช้ที่มีการพิสูจน์ตัวจริง ตัวแทนลูกค้า (หรือที่คุณเลือก)</span><span class="sxs-lookup"><span data-stu-id="35920-129">**Web roles**: Authenticated Users, Customer Representative (or your choice)</span></span>

5. <span data-ttu-id="35920-130">สร้างและบันทึกสิทธิ์ใหม่สำหรับการเชื่อมต่อของฝ่ายไปยังบัญชี โดยตั้งค่าพารามิเตอร์เหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="35920-130">Create and save a new permission for the Party to Account connection, setting these parameters:</span></span>

    + <span data-ttu-id="35920-131">**ชื่อ**: การเชื่อมต่อของฝ่ายไปยังบัญชี (หรือที่คุณเลือก)</span><span class="sxs-lookup"><span data-stu-id="35920-131">**Name**: Party to Account Connection (or your choice)</span></span>
    + <span data-ttu-id="35920-132">**ชื่อตาราง**: บัญชี</span><span class="sxs-lookup"><span data-stu-id="35920-132">**Table Name**: account</span></span>
    + <span data-ttu-id="35920-133">**เว็บไซต์**: พอร์ทัลของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="35920-133">**Website**: Customer Portal</span></span>
    + <span data-ttu-id="35920-134">**ขอบเขต**: ข้อมูลหลัก</span><span class="sxs-lookup"><span data-stu-id="35920-134">**Scope**: Parent</span></span>
    + <span data-ttu-id="35920-135">**สิทธิ์**: เลือกทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="35920-135">**Privileges**: Select all</span></span>
    + <span data-ttu-id="35920-136">**สิทธิ์ของตารางหลัก**: การเชื่อมต่อของผู้ติดต่อไปยังฝ่าย</span><span class="sxs-lookup"><span data-stu-id="35920-136">**Parent Table Permission**: Contact to Party Connection</span></span>

6. <span data-ttu-id="35920-137">สร้างและบันทึกสิทธิ์ใหม่สำหรับการเชื่อมต่อของบัญชีไปยังใบสั่ง โดยตั้งค่าพารามิเตอร์เหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="35920-137">Create and save a new permission for the Account to Order connection, setting these parameters:</span></span>

    + <span data-ttu-id="35920-138">**ชื่อ**: การเชื่อมต่อของบัญชีไปยังใบสั่ง (หรือที่คุณเลือก)</span><span class="sxs-lookup"><span data-stu-id="35920-138">**Name**: Account to Order Connection (or your choice)</span></span>
    + <span data-ttu-id="35920-139">**ชื่อตาราง**: salesorder</span><span class="sxs-lookup"><span data-stu-id="35920-139">**Table Name**: salesorder</span></span>
    + <span data-ttu-id="35920-140">**เว็บไซต์**: พอร์ทัลของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="35920-140">**Website**: Customer Portal</span></span>
    + <span data-ttu-id="35920-141">**ขอบเขต**: ข้อมูลหลัก</span><span class="sxs-lookup"><span data-stu-id="35920-141">**Scope**: Parent</span></span>
    + <span data-ttu-id="35920-142">**สิทธิ์**: เลือกทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="35920-142">**Privileges**: Select all</span></span>
    + <span data-ttu-id="35920-143">**สิทธิ์ของตารางหลัก**: การเชื่อมต่อของฝ่ายไปยังบัญชี</span><span class="sxs-lookup"><span data-stu-id="35920-143">**Parent Table Permission**: Party to Account Connection</span></span>

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
