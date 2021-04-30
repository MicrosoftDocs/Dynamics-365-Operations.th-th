---
title: แก้ไขการอัปเกรดและการโยกย้ายไปที่การจัดการคลังสินค้าขั้นสูง
description: หัวข้อนี้อธิบายวิธีการแก้ไขปัญหาทั่วไปที่คุณอาจพบในระหว่างที่คุณอัปเกรดและการโยกย้ายไปที่การจัดการคลังสินค้าขั้นสูง
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 12dcadae2a65d71614a2eee9468ec93cac284a7b
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/16/2021
ms.locfileid: "5907898"
---
# <a name="troubleshoot-upgrade-and-migration-to-advanced-warehouse-management"></a><span data-ttu-id="e71eb-103">แก้ไขการอัปเกรดและการโยกย้ายไปที่การจัดการคลังสินค้าขั้นสูง</span><span class="sxs-lookup"><span data-stu-id="e71eb-103">Troubleshoot upgrade and migration to advanced warehouse management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e71eb-104">หัวข้อนี้อธิบายวิธีการแก้ไขปัญหาทั่วไปที่คุณอาจพบในระหว่างที่คุณอัปเกรดและการโยกย้ายไปที่การจัดการคลังสินค้าขั้นสูง</span><span class="sxs-lookup"><span data-stu-id="e71eb-104">This topic describes how to fix common issues that you might encounter while you upgrade and migrate to advanced warehouse management.</span></span>

## <a name="i-receive-the-following-error-message-javasecuritycertcertpathvalidatorexception-trust-anchor-for-certification-path-is-not-found"></a><span data-ttu-id="e71eb-105">ฉันได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้: "java.security.cert.certPathValidatorException: ไม่พบจุดยึดของความเชื่อถือสำหรับเส้นทางใบรับรอง"</span><span class="sxs-lookup"><span data-stu-id="e71eb-105">I receive the following error message: "java.security.cert.certPathValidatorException: Trust anchor for certification path is not found."</span></span>

### <a name="issue-description"></a><span data-ttu-id="e71eb-106">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="e71eb-106">Issue description</span></span>

<span data-ttu-id="e71eb-107">คุณได้รับข้อความแสดงข้อความในแอปการจัดการคลังสินค้าบนมือถือ เนื่องจากใบรับรองที่มีการลงชื่อด้วยตนเองไม่ได้รับความไว้วางใจในสภาพแวดล้อม Android 8+ ในสถานที่</span><span class="sxs-lookup"><span data-stu-id="e71eb-107">You receive this error message in the Warehouse Management mobile app, because self-signed certificates aren't trusted on Android 8+ in on-premises environments.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="e71eb-108">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="e71eb-108">Issue resolution</span></span>

<span data-ttu-id="e71eb-109">ใช้หน่วยงานรับรองภายนอก (สาธารณะ) (CA)</span><span class="sxs-lookup"><span data-stu-id="e71eb-109">Use an external (public) certifying authority (CA).</span></span> <span data-ttu-id="e71eb-110">การแก้ไขสำหรับปัญหานี้จะพร้อมใช้งานในรุ่น 1.9.0.0 ของแอปคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="e71eb-110">A fix for this issue is available in version 1.9.0.0 of the warehouse app.</span></span> <span data-ttu-id="e71eb-111">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการตัดสินค้าจากคลังและวิธีการแก้ไข ให้ดูที่ [แก้ไขปัญหาเกี่ยวกับการเชื่อมต่อของแอปการจัดการคลังสินค้าบนมือถือ](troubleshoot-warehouse-app-connection.md)</span><span class="sxs-lookup"><span data-stu-id="e71eb-111">For more information about this issue and how to fix it, see [Troubleshoot Warehouse Management mobile app connection issues](troubleshoot-warehouse-app-connection.md).</span></span>

## <a name="what-is-the-approved-process-for-moving-from-basic-warehousing-to-advanced-warehousing"></a><span data-ttu-id="e71eb-112">กระบวนการที่ได้รับการอนุมัติสำหรับการเคลื่อนย้ายจากคลังสินค้าขั้นพื้นฐานไปยังคลังสินค้าขั้นสูงมีอะไรบ้าง</span><span class="sxs-lookup"><span data-stu-id="e71eb-112">What is the approved process for moving from basic warehousing to advanced warehousing?</span></span>

### <a name="issue-description"></a><span data-ttu-id="e71eb-113">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="e71eb-113">Issue description</span></span>

<span data-ttu-id="e71eb-114">ขณะนี้คุณกำลังทำงานอยู่ภายใต้การบริหารสต็อก/สินค้าคงคลังและการใช้ฟังก์ชันการทำงานพื้นฐานของสินค้าคงคลัง และคุณต้องการย้ายไปยังคลังสินค้าขั้นสูงเพื่อใช้ประโยชน์จากอุปกรณ์เคลื่อนที่ เวฟ และงาน</span><span class="sxs-lookup"><span data-stu-id="e71eb-114">You're currently running under stock/inventory management and using basic stock functionality, and you want to move to advanced warehousing to take advantage of mobile devices, waves, and work.</span></span> <span data-ttu-id="e71eb-115">อย่างไรก็ตาม คุณกำลังประสบปัญหาเมื่อคุณพยายามทำการย้าย</span><span class="sxs-lookup"><span data-stu-id="e71eb-115">However, you're experiencing issues when you try to make this move.</span></span> <span data-ttu-id="e71eb-116">ตัวอย่างเช่น คุณไม่สามารถเปลี่ยนผลิตภัณฑ์ของคุณเพื่อให้ใช้มิติการจัดเก็บ (ไซต์ คลังสินค้า และสถานที่เก็บ) เนื่องจากผลิตภัณฑ์มีธุรกรรมอยู่</span><span class="sxs-lookup"><span data-stu-id="e71eb-116">For example, you can't change your products so that they use storage dimensions (site, warehouse, and location), because the products have transactions against them.</span></span> <span data-ttu-id="e71eb-117">ดังนั้น คุณต้องเรียนรู้กระบวนการที่ได้รับการอนุมัติสำหรับการเคลื่อนย้ายจากคลังสินค้าขั้นพื้นฐานไปยังคลังสินค้าขั้นสูง</span><span class="sxs-lookup"><span data-stu-id="e71eb-117">Therefore, you must learn the approved process for moving from basic warehousing to advanced warehousing.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="e71eb-118">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="e71eb-118">Issue resolution</span></span>

<span data-ttu-id="e71eb-119">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับกระบวนการสำหรับการย้ายจากคลังสินค้าพื้นฐานไปยังคลังสินค้าขั้นสูง ให้ดูที่การลงรายการบัญชีและเอกสารต่อไปนี้ของบล็อก:</span><span class="sxs-lookup"><span data-stu-id="e71eb-119">For more information about the process for moving from basic warehousing to advanced warehousing, see the following blog posts and documentation:</span></span>

- [<span data-ttu-id="e71eb-120">เปิดใช้งานสำหรับกระบวนการบริหารคลังสินค้าสำหรับสินค้าและคลังสินค้าที่มี</span><span class="sxs-lookup"><span data-stu-id="e71eb-120">Enable warehouse management process for existing items and warehouses</span></span>](https://cleverax.wordpress.com/2017/12/06/d365fo-enable-warehouse-management-process-for-existing-items-and-warehouses/)
- [<span data-ttu-id="e71eb-121">การโยกย้ายของ Microsoft Dynamics AX WMS ไปยังคลังสินค้า R3 ใหม่และฟังก์ชันการขนส่ง</span><span class="sxs-lookup"><span data-stu-id="e71eb-121">Migration of Microsoft Dynamics AX WMS to new R3 warehouse and transportation functionality</span></span>](https://cloudblogs.microsoft.com/dynamics365/no-audience/2015/08/17/migration-of-microsoft-dynamics-ax-wms-to-new-r3-warehouse-and-transportation-functionality/)
- [<span data-ttu-id="e71eb-122">การย้ายสินค้า WMSI/WMS2</span><span class="sxs-lookup"><span data-stu-id="e71eb-122">WMSI/WMS2 item migration</span></span>](https://cloudblogs.microsoft.com/dynamics365/no-audience/2018/05/03/wmsiwms2-item-migration/)
- [<span data-ttu-id="e71eb-123">อัพเกรดการจัดการคลังสินค้าจาก Microsoft Dynamics AX 2012 ไปยัง Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="e71eb-123">Upgrade warehouse management from Microsoft Dynamics AX 2012 to Supply Chain Management</span></span>](./upgrade-migration-warehouse-management-processes.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]