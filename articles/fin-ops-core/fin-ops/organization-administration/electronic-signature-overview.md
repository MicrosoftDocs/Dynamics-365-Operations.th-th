---
title: ภาพรวมของลายเซ็นอิเล็กทรอนิกส์
description: บทความนี้ให้ภาพรวมของลายเซ็นอิเล็กทรอนิกส์และอธิบายวิธีการที่สามารถใช้งานได้
author: maertenm
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SIGParameters, SIGProcSetup, SIGReasonCode
audience: Application User
ms.reviewer: sericks
ms.custom: 13611
ms.assetid: 98dc6b79-1895-45d8-9dd1-2c8a351b58af
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 051bb023d3456dae0be30de3897b282c2d50c5af
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/19/2020
ms.locfileid: "4797639"
---
# <a name="electronic-signatures-overview"></a><span data-ttu-id="90d3a-103">ภาพรวมของลายเซ็นอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="90d3a-103">Electronic signatures overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="90d3a-104">บทความนี้ให้ภาพรวมของลายเซ็นอิเล็กทรอนิกส์และอธิบายวิธีการที่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="90d3a-104">This article provides an overview of electronic signatures and describes how they can be used.</span></span>

## <a name="what-is-an-electronic-signature"></a><span data-ttu-id="90d3a-105">ลายเซ็นอิเล็กทรอนิกส์คืออะไร?</span><span class="sxs-lookup"><span data-stu-id="90d3a-105">What is an electronic signature?</span></span>

<span data-ttu-id="90d3a-106">ลายเซ็นอิเล็กทรอนิกส์จะยืนยันลักษณะเฉพาะของบุคคลที่กำลังจะเริ่มหรืออนุมัติกระบวนการระบบคอมพิวเตอร์ </span><span class="sxs-lookup"><span data-stu-id="90d3a-106">An electronic signature confirms the identity of a person who is about to start or approve a computing process.</span></span> <span data-ttu-id="90d3a-107">ในบางอุตสาหกรรม ลายเซ็นอิเล็กทรอนิกส์เป็นการผูกมัดตามกฎหมายเสมือนลายเซ็นที่เป็นลายมือ</span><span class="sxs-lookup"><span data-stu-id="90d3a-107">In some industries, an electronic signature is as legally binding as a handwritten signature.</span></span>

<span data-ttu-id="90d3a-108">ลายเซ็นอิเล็กทรอนิกส์เป็นข้อกำหนดของข้อบังคับที่ต้องปฏิบัติตามสำหรับอุตสาหกรรมต่าง ๆ เช่นอุตสาหกรรมยา อาหารและเครื่องดื่ม และอุตสาหกรรมอวกาศ และความมั่นคง</span><span class="sxs-lookup"><span data-stu-id="90d3a-108">Electronic signatures are a regulations compliance requirement for several regulated industries, such as pharmaceuticals, food and beverage, and aerospace and defense.</span></span> <span data-ttu-id="90d3a-109">ยังเป็นส่วนสำคัญของข้อบังคับที่ต้องปฏิบัติตามภายใต้ระเบียบ 21 CFR Part 11 ที่ออกโดยองค์การอาหารและยา (FDA) ของสหรัฐอเมริกา</span><span class="sxs-lookup"><span data-stu-id="90d3a-109">They are also required for compliance with regulations in 21 CFR Part 11 that was issued by the Food and Drug Administration (FDA) in the United States.</span></span>

> [!NOTE]
> <span data-ttu-id="90d3a-110">ตัวลายเซ็นอิเล็กทรอนิกส์เองไม่เหมือนกับลายเซ็นดิจิทัล</span><span class="sxs-lookup"><span data-stu-id="90d3a-110">An electronic signature by itself isn't the same as a digital signature.</span></span> <span data-ttu-id="90d3a-111">ลายเซ็นอิเล็กทรอนิกส์เป็นเพียงสิ่งที่ใช้ทดแทนลายเซ็นที่เป็นลายมือ ในขณะที่ลายเซ็นดิจิทัลเป็นมาตรการรักษาความปลอดภัยเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="90d3a-111">An electronic signature is just a substitute for a handwritten signature, whereas a digital signature provides additional security measures.</span></span> <span data-ttu-id="90d3a-112">ลายเซ็นดิจิทัลสามารถช่วยระบุว่าผู้ใช้หรือกระบวนการอื่นได้แอบแก้ไขข้อมูลหรือไม่</span><span class="sxs-lookup"><span data-stu-id="90d3a-112">A digital signature can help identify whether another user or process has tampered with the data.</span></span> <span data-ttu-id="90d3a-113">ลายเซ็นดิจิทัลยังสามารถตรวจสอบ และการตรวจสอบนี้ไม่สามารถโต้แย้งโดยเจ้าของใบรับรองที่เคยลงชื่อในข้อมูลได้</span><span class="sxs-lookup"><span data-stu-id="90d3a-113">A digital signature can also be verified, and this verification can't be refuted by the owner of the certificate that was used to sign the data.</span></span> <span data-ttu-id="90d3a-114">ดังที่อธิบายไว้ข้างล่างนี้ ลายเซ็นอิเล็กทรอนิกส์ มีฟังก์ชันลายเซ็นดิจิทัลในตัว</span><span class="sxs-lookup"><span data-stu-id="90d3a-114">As described below, electronic signatures have built-in digital signature functionality.</span></span>

## <a name="electronic-signatures"></a><span data-ttu-id="90d3a-115">ลายเซ็นอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="90d3a-115">Electronic signatures</span></span>

<span data-ttu-id="90d3a-116">คุณสามารถใช้ลายเซ็นอิเล็กทรอนิกส์สำหรับกระบวนการทางธุรกิจที่สำคัญได้</span><span class="sxs-lookup"><span data-stu-id="90d3a-116">You can use electronic signatures for critical business processes.</span></span> <span data-ttu-id="90d3a-117">บางกระบวนการมีความสามารถด้านลายเซ็นอิเล็กทรอนิกส์ในตัว</span><span class="sxs-lookup"><span data-stu-id="90d3a-117">Some processes have built-in electronic signature capabilities.</span></span> <span data-ttu-id="90d3a-118">คุณยังสามารถสร้างข้อกำหนดของลายเซ็นที่กำหนดเองสำหรับตารางฐานข้อมูลและฟิลด์ใดๆ</span><span class="sxs-lookup"><span data-stu-id="90d3a-118">You can also create custom signature requirements for any database table and field.</span></span>

<span data-ttu-id="90d3a-119">ลายเซ็นอิเล็กทรอนิกส์มีความสามารถด้านลายเซ็นดิจิทัลในตัว</span><span class="sxs-lookup"><span data-stu-id="90d3a-119">Electronic signatures have built-in digital signature functionality.</span></span> <span data-ttu-id="90d3a-120">ผู้ใช้ทุกรายที่ลงชื่อในเอกสารต้องต้องจัดหาใบรับรองการเข้ารหัสลับที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="90d3a-120">Every user who signs documents must obtain a valid cryptographic certificate.</span></span> <span data-ttu-id="90d3a-121">เมื่อเอกสารถูกลงชื่อ คีย์ส่วนตัวเชื่อมโยงกับใบรับรองที่ได้รับการตรวจสอบความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="90d3a-121">When a document is signed, the private key that is associated with that certificate is validated.</span></span> <span data-ttu-id="90d3a-122">ลายเซ็นอิเล็กทรอนิกส์ถูกบันทึกไว้ในล็อก เพื่อเป็นข้อมูลสำหรับบันทึกการตรวจสอบบัญชี</span><span class="sxs-lookup"><span data-stu-id="90d3a-122">Electronic signature information is recorded in a log to provide an audit trail.</span></span> <span data-ttu-id="90d3a-123">เมื่อต้องการตั้งค่าลายเซ็นอิเล็กทรอนิกส์ ดู [ตั้งค่าลายเซ็นอิเล็กทรอนิกส์](tasks/set-up-electronic-signatures.md)</span><span class="sxs-lookup"><span data-stu-id="90d3a-123">To set up electronic signatures, see [Set up electronic signatures](tasks/set-up-electronic-signatures.md).</span></span>

## <a name="users-who-require-access-to-electronic-signatures"></a><span data-ttu-id="90d3a-124">ผู้ใช้ที่ต้องการเข้าถึงลายเซ็นอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="90d3a-124">Users who require access to electronic signatures</span></span>

<span data-ttu-id="90d3a-125">โดยทั่วไปผู้ใช้สามชนิดต้องใช้การเข้าถึงที่ปลอดภัยไปยังลายเซ็นอิเล็กทรอนิกส์ ได้แก่ ผู้ดูแลลายเซ็นอิเล็กทรอนิกส์ ผู้ลงชื่อ และผู้ตรวจสอบลายเซ็นอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="90d3a-125">Three kinds of users typically require security access to electronic signatures: electronic signature administrators, signers, and electronic signature auditors.</span></span>

### <a name="electronic-signature-administrator"></a><span data-ttu-id="90d3a-126">ผู้ดูแลลายเซ็นอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="90d3a-126">Electronic signature administrator</span></span>

<span data-ttu-id="90d3a-127">ผู้ดูแลระบบลายเซ็นอิเล็กทรอนิกส์ตั้งค่าข้อกำหนดของลายเซ็น พารามิเตอร์ทั่วไป และผู้อนุมัติ และได้รับการแจ้งเตือนเมื่อลายเซ็นไม่สามารถตรวจสอบได้</span><span class="sxs-lookup"><span data-stu-id="90d3a-127">The electronic signature administrator sets up signature requirements, general parameters, and approvers, and receives alerts when signatures can't be verified.</span></span> <span data-ttu-id="90d3a-128">โดยค่าเริ่มต้น ผู้ใช้ที่เป็นสมาชิก **ผู้จัดการฝ่ายเทคโนโลยีสารสนเทศ** บทบาทความปลอดภัยมีสิทธิ์เพื่อดูแลลายเซ็นอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="90d3a-128">By default, a user who belongs to the **Information technology manager** security role has permission to administer electronic signatures.</span></span>

### <a name="signer"></a><span data-ttu-id="90d3a-129">ผู้ลงชื่อ</span><span class="sxs-lookup"><span data-stu-id="90d3a-129">Signer</span></span>

<span data-ttu-id="90d3a-130">ผู้ลงชื่อแสดงลายเซ็นอิเล็กทรอนิกส์สำหรับเอกสารและกระบวนการที่ต้องการลายเซ็น</span><span class="sxs-lookup"><span data-stu-id="90d3a-130">A signer provides electronic signatures for documents and processes that require signatures.</span></span> <span data-ttu-id="90d3a-131">โดยค่าเริ่มต้น ผู้ใช้ที่เป็นสมาชิก **ผู้ใช้ระบบ** บทบาทความปลอดภัยมีสิทธิ์เพื่อลงชื่อในเอกสารทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="90d3a-131">By default, a user who belongs to the **System user** security role has permission to sign documents electronically.</span></span>

> [!NOTE]
> <span data-ttu-id="90d3a-132">ผู้ลงชื่ออาจต้องมีสิทธิ์เพิ่มเติมก่อนที่จะได้รับอนุญาตให้เข้าถึงข้อมูลที่เกี่ยวข้องกับเอกสารหรือกระบวนการที่กำลังลงชื่ออยู่</span><span class="sxs-lookup"><span data-stu-id="90d3a-132">The signer might require additional permissions before access is granted to data that is related to the document or process that is being signed.</span></span> <span data-ttu-id="90d3a-133">ผู้ใช้ที่เปลี่ยนข้อมูล และจากนั้นต้องลงชื่อสำหรับการเปลี่ยนแปลงเหล่านั้น ต้องมีสิทธิ์เพื่อเปลี่ยนแปลงข้อมูล</span><span class="sxs-lookup"><span data-stu-id="90d3a-133">A user who changes data and must then sign for those changes must have permission to change the data.</span></span> <span data-ttu-id="90d3a-134">ผู้ใช้ที่ลงชื่อในนามของผู้ใช้อื่นอาจไม่จำเป็นต้องเข้าถึงข้อมูล</span><span class="sxs-lookup"><span data-stu-id="90d3a-134">A user who signs on behalf of another user might not require access to the data.</span></span> <span data-ttu-id="90d3a-135">ตัวอย่างของชนิดของผู้ใช้นี้เป็นผู้ควบคุมงานที่ลงชื่อสำหรับการเปลี่ยนแปลงของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="90d3a-135">An example of this kind of user is a supervisor who signs for an employee's changes.</span></span>

### <a name="electronic-signature-auditor"></a><span data-ttu-id="90d3a-136">ผู้ตรวจสอบลายเซ็นอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="90d3a-136">Electronic signature auditor</span></span>

<span data-ttu-id="90d3a-137">ผู้ตรวจสอบลายเซ็นอิเล็กทรอนิกส์ตรวจทานล็อกฐานข้อมูลและล็อกการตรวจทานลายเซ็นที่พร้อมใช้งานจากล็อกฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="90d3a-137">The electronic signature auditor reviews the database log and the signature review log that is available from the database log.</span></span> <span data-ttu-id="90d3a-138">โดยค่าเริ่มต้น ผู้ใช้ที่เป็นสมาชิก **ผู้จัดการฝ่ายเทคโนโลยีสารสนเทศ** บทบาทความปลอดภัยมีสิทธิ์เพื่อตรวจสอบลายเซ็นอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="90d3a-138">By default, a user who belongs to the **Information technology manager** security role has permission to audit electronic signatures.</span></span>

<span data-ttu-id="90d3a-139">ถ้าคุณใช้บทบาทอื่นมากกว่า **ผู้จัดการฝ่ายเทคโนโลยีสารสนเทศ** ทำให้แน่ใจว่าบทบาทถูกกำหนดสิทธิ์ต่อไปนี้แล้ว:</span><span class="sxs-lookup"><span data-stu-id="90d3a-139">If you use a role other than **Information technology manager**, make sure that the role is assigned the following privileges:</span></span>

- <span data-ttu-id="90d3a-140">ดูความล้มเหลวของลายเซ็นอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="90d3a-140">View electronic signature failures</span></span>
- <span data-ttu-id="90d3a-141">ดูล็อกฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="90d3a-141">View database log</span></span>

## <a name="signing-documents-electronically"></a><span data-ttu-id="90d3a-142">การลงชื่อในเอกสารทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="90d3a-142">Signing documents electronically</span></span>

### <a name="get-a-certificate"></a><span data-ttu-id="90d3a-143">การขอใบรับรอง</span><span class="sxs-lookup"><span data-stu-id="90d3a-143">Get a certificate</span></span>

<span data-ttu-id="90d3a-144">ก่อนที่คุณจะลงชื่อในเอกสารทางอิเล็กทรอนิกส์ คุณจะต้องขอใบรับรอง</span><span class="sxs-lookup"><span data-stu-id="90d3a-144">Before you sign documents electronically, you must request a certificate.</span></span>

> [!NOTE]
> <span data-ttu-id="90d3a-145">คุณลักษณะ Microsoft SQL Server ถูกใช้เพื่อสร้างใบรับรองและเปิดใช้งานการลงชื่อทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="90d3a-145">Microsoft SQL Server features are used to create certificates and enable electronic signing.</span></span> <span data-ttu-id="90d3a-146">ไม่จำเป็นต้องใช้ใบรับรองหรือโครงสร้างพื้นฐานคีย์สาธารณะ (PKI) เพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="90d3a-146">No additional certificate or public key infrastructure (PKI) is required.</span></span>

<span data-ttu-id="90d3a-147">เมื่อคุณขอใบรับรอง จะมีการสร้างคีย์สาธารณะและคีย์ส่วนตัวให้แก่คุณ</span><span class="sxs-lookup"><span data-stu-id="90d3a-147">When you request a certificate, a public key and a private key are created for you.</span></span> <span data-ttu-id="90d3a-148">คีย์ส่วนตัวจะถูกเข้ารหัสลับโดยใช้รหัสผ่านที่มีคุณเท่านั้นที่ทราบ</span><span class="sxs-lookup"><span data-stu-id="90d3a-148">The private key is encrypted by using a password that is known only to you.</span></span> <span data-ttu-id="90d3a-149">เมื่อคุณลงชื่อในเอกสารทางอิเล็กทรอนิกส์ จะมีการตรวจสอบความถูกต้องสำหรับข้อมูลประจำตัวของคุณเมื่อคุณป้อนรหัสผ่าน</span><span class="sxs-lookup"><span data-stu-id="90d3a-149">When you sign a document electronically, your identity is verified when you enter the password.</span></span>

<span data-ttu-id="90d3a-150">เมื่อต้องการร้องขอใบรับรอง ที่หน้า **ตัวเลือก** บนแท็บ **บัญชี** คลิก **ขอใบรับรอง**</span><span class="sxs-lookup"><span data-stu-id="90d3a-150">To request a certificate, on the **Options** page, on the **Accounts** tab, click **Get certificate**.</span></span>

<span data-ttu-id="90d3a-151">คุณจะต้องป้อนและยืนยันรหัสผ่านที่คุณจะใช้สำหรับการลงชื่อ</span><span class="sxs-lookup"><span data-stu-id="90d3a-151">You must enter and confirm the password that you will use for signing.</span></span> <span data-ttu-id="90d3a-152">รหัสผ่านใช้เพื่อป้องกันคีย์ส่วนตัวของคุณและอนุมัติการใช้ใบรับรองของคุณ</span><span class="sxs-lookup"><span data-stu-id="90d3a-152">The password is used to protect your private key and authorize the use of your certificate.</span></span> <span data-ttu-id="90d3a-153">รหัสผ่านนี้ไม่มีการจัดเก็บไว้ในฐานข้อมูล และบุคคลอื่นไม่สามารถใช้ได้ แม้แต่ผู้ดูแลระบบก็ตาม</span><span class="sxs-lookup"><span data-stu-id="90d3a-153">This password isn't stored in the database, and it isn't available to anyone else, not even to the administrator.</span></span>

<span data-ttu-id="90d3a-154">ถ้าคุณลืมรหัสผ่านที่เชื่อมโยงกับใบรับรองของคุณ จะต้องตั้งค่าใบรับรองนั้นใหม่</span><span class="sxs-lookup"><span data-stu-id="90d3a-154">If you forget the password that is connected with your certificate, that certificate must be reset.</span></span> <span data-ttu-id="90d3a-155">ถ้าคุณตั้งค่าใบรับรอง คุณจะส่งผลกระทบต่อเอกสารที่คุณลงชื่อโดยใช้ใบรับรองก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="90d3a-155">If you reset the certificate, you don't affect documents that you signed by using the previous certificate.</span></span> <span data-ttu-id="90d3a-156">เมื่อต้องการรีเซ็ตใบรับรอง ในหน้า **ตัวเลือก** คลิก **รีเซ็ตใบรับรอง**</span><span class="sxs-lookup"><span data-stu-id="90d3a-156">To reset the certificate, on the **Options** page, click **Reset certificate**.</span></span>

### <a name="sign-a-document-electronically"></a><span data-ttu-id="90d3a-157">การลงชื่อในเอกสารทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="90d3a-157">Sign a document electronically</span></span>

<span data-ttu-id="90d3a-158">หน้า **ลงชื่อในเอกสาร** จะแสดงขึ้น เมื่อคุณทำการเปลี่ยนแปลงที่ต้องใช้ลายเซ็นอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="90d3a-158">The **Sign document** page is displayed when you make a change that requires an electronic signature.</span></span>

1. <span data-ttu-id="90d3a-159">ในหน้า **ลงชื่อเอกสาร** คลิกแท็บ **เอกสาร** เพื่อตรวจทานการเปลี่ยนแปลงในเอกสาร</span><span class="sxs-lookup"><span data-stu-id="90d3a-159">On the **Sign document** page, click the **Document** tab to review the changes to the document.</span></span>
2. <span data-ttu-id="90d3a-160">บนแท็บ **ลายเซ็น** ให้เลือกรหัสเหตุผล</span><span class="sxs-lookup"><span data-stu-id="90d3a-160">On the **Signature** tab, select a reason code.</span></span>
3. <span data-ttu-id="90d3a-161">ป้อนข้อคิดเห็น ถ้าจำเป็นต้องมีข้อคิดเห็น</span><span class="sxs-lookup"><span data-stu-id="90d3a-161">Enter a comment, if a comment is required.</span></span>
4. <span data-ttu-id="90d3a-162">ถ้ารหัสผู้ใช้ของคุณไม่แสดงขึ้นในฟิลด์ **ผู้ลงชื่อ** ให้เลือกรหัสผู้ใช้ในรายการ</span><span class="sxs-lookup"><span data-stu-id="90d3a-162">If your user ID doesn't appear in the **Signer** field, select it in the list.</span></span>
5. <span data-ttu-id="90d3a-163">ป้อนที่ตั้งของคุณ ถ้าจำเป็นต้องมีข้อมูลนี้</span><span class="sxs-lookup"><span data-stu-id="90d3a-163">Enter your location, if this information is required.</span></span>
6. <span data-ttu-id="90d3a-164">คลิก **ตกลง** ระบบจะนำเข้าข้อมูลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="90d3a-164">Click **OK**.</span></span>

### <a name="sign-for-another-users-changes"></a><span data-ttu-id="90d3a-165">ลงชื่อสำหรับการเปลี่ยนแปลงของผู้ใช้รายอื่น</span><span class="sxs-lookup"><span data-stu-id="90d3a-165">Sign for another user's changes</span></span>

<span data-ttu-id="90d3a-166">บางครั้งคุณอาจต้องการให้ผู้ใช้ลงชื่อสำหรับการเปลี่ยนแปลงของผู้ใช้รายอื่น</span><span class="sxs-lookup"><span data-stu-id="90d3a-166">Occasionally, you might want a user to sign for another user's changes.</span></span> <span data-ttu-id="90d3a-167">ตัวอย่างเช่น ผู้ควบคุมงานอาจจำเป็นต้องลงชื่อสำหรับการเปลี่ยนแปลงที่พนักงานทำรายการในสูตรการผลิต (BOM)</span><span class="sxs-lookup"><span data-stu-id="90d3a-167">For example, a supervisor might be required to sign for changes that an employee makes to a bill of materials (BOM).</span></span> <span data-ttu-id="90d3a-168">ใช้ขั้นตอนนี้เพื่อแต่งตั้งผู้ใช้ เป็นผู้ลงชื่อสำหรับผู้ใช้รายอื่น</span><span class="sxs-lookup"><span data-stu-id="90d3a-168">Use this procedure to designate a user as a signer for another user.</span></span>

> [!NOTE]
> <span data-ttu-id="90d3a-169">เมื่อผู้ใช้หนึ่งรายลงชื่อสำหรับการเปลี่ยนแปลงของผู้ใช้รายอื่น ต้องมีการให้ลายเซ็นไว้ที่เวิร์กสเตชันของผู้ใช้ที่เป็นผู้ทำการเปลี่ยนแปลง </span><span class="sxs-lookup"><span data-stu-id="90d3a-169">When one user signs for another user's change, the signature must be provided at the workstation of the user who made the change.</span></span> <span data-ttu-id="90d3a-170">ผู้ใช้ไม่สามารถบันทึกการเปลี่ยนแปลงได้จนกว่าจะมีลายเซ็น</span><span class="sxs-lookup"><span data-stu-id="90d3a-170">The user can't save the change until the signature has been provided.</span></span>

<span data-ttu-id="90d3a-171">เมื่อต้องการแต่งตั้งผู้อนุมัติ ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="90d3a-171">To designate approvers, follow these steps.</span></span>

1. <span data-ttu-id="90d3a-172">ในหน้า **ตัวเลือก** บนแท็บ **บัญชี** คลิก **แต่งตั้งผู้อนุมัติ**</span><span class="sxs-lookup"><span data-stu-id="90d3a-172">On the **Options** page, on the **Accounts** tab, click **Designate approver**.</span></span>
2. <span data-ttu-id="90d3a-173">ในฟิลด์ **รหัสผู้ใช้ของผู้อนุมัติ** ให้เลือกรหัสของผู้ใช้ที่ต้องลงชื่อสำหรับการเปลี่ยนแปลงของผู้ใช้รายอื่น</span><span class="sxs-lookup"><span data-stu-id="90d3a-173">In the **Approver user ID** field, select the ID of the user who must sign for another user's changes.</span></span>
3. <span data-ttu-id="90d3a-174">ในฟิลด์ **ลงชื่อเพื่อขอรหัสผู้ใช้** ให้เลือกรหัสของผู้ใช้ที่เป็นเจ้าของการเปลี่ยนแปลงที่ต้องได้รับการลงชื่อ</span><span class="sxs-lookup"><span data-stu-id="90d3a-174">In the **Sign for user ID** field, select the ID of the user whose changes must be signed for.</span></span>
