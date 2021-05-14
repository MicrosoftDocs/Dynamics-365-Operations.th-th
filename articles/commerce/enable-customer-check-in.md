---
title: เปิดใช้งานการแจ้งเตือนการเช็คอินของลูกค้าในการขายหน้าร้าน (POS)
description: หัวข้อนี้จะอธิบายวิธีการเปิดใช้งานการแจ้งเตือนการเช็คอินของลูกค้าในการขายหน้าร้านของ Microsoft Dynamics 365 Commerce (POS)
author: bicyclingfool
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: e4defc15d9ef198a361934d51e31016747dbb5ab
ms.sourcegitcommit: 593438a145672c55ff6a910eabce2939300b40ad
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/23/2021
ms.locfileid: "5937621"
---
# <a name="enable-customer-check-in-notifications-in-point-of-sale-pos"></a><span data-ttu-id="4ec80-103">เปิดใช้งานการแจ้งเตือนการเช็คอินของลูกค้าในการขายหน้าร้าน (POS)</span><span class="sxs-lookup"><span data-stu-id="4ec80-103">Enable customer check-in notifications in point of sale (POS)</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="4ec80-104">หัวข้อนี้จะอธิบายวิธีการเปิดใช้งานการแจ้งเตือนการเช็คอินของลูกค้าในการขายหน้าร้านของ Microsoft Dynamics 365 Commerce (POS)</span><span class="sxs-lookup"><span data-stu-id="4ec80-104">This topic describes how to enable customer check-in notifications in Microsoft Dynamics 365 Commerce point of sale (POS).</span></span>

<span data-ttu-id="4ec80-105">ในอีเมล "ใบสั่งที่พร้อมสำหรับจัดส่ง" องค์กรสามารถระบุลิงค์หรือปุ่มที่ทำให้ลูกค้าแจ้งร้านค้าว่าลูกค้าอยู่ในองค์กรและรอให้บรรจุภัณฑ์ถูกเบิกออกมา</span><span class="sxs-lookup"><span data-stu-id="4ec80-105">In their "order ready for pickup" emails, organizations can provide a link or button that lets customers notify the store that they are on the premises and waiting for their package to be brought out to them.</span></span> <span data-ttu-id="4ec80-106">จากนั้น ลูกค้าจะได้รับการยืนยันการเช็คอิน และร้านค้าจะได้รับการแจ้งเตือนเป็นงานในแอปพลิเคชัน POS</span><span class="sxs-lookup"><span data-stu-id="4ec80-106">Customers then receive a check-in confirmation, and the store receives a notification as a task in its POS application.</span></span> <span data-ttu-id="4ec80-107">งานนี้ทำหน้าที่เป็นพร้อมต์สำหรับการเชื่อมโยงการขายเพื่อจัดส่งสินค้าตามใบสั่งไปยังพาหนะของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="4ec80-107">This task serves as a prompt for a sales associate to deliver the order to the customer's vehicle.</span></span> <span data-ttu-id="4ec80-108">ดังนั้น ลูกค้าจึงไม่ต้องเข้ามาในร้านค้า</span><span class="sxs-lookup"><span data-stu-id="4ec80-108">Therefore, the customer doesn't have to enter the store.</span></span>

<span data-ttu-id="4ec80-109">นอกจากนี้ ลำดับงานการเช็คอินของลูกค้ายังสามารถถูกตั้งค่าคอนฟิกให้รวบรวมข้อมูลเพิ่มเติมจากลูกค้าได้ด้วย เช่น หมายเลขจุดจอดรถ รุ่น และสีรถ และคําแนะนําในการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="4ec80-109">The customer check-in workflow can also be configured to collect additional information from customers, such as their parking spot number, the make, model, and color of their vehicle, and delivery instructions.</span></span> <span data-ttu-id="4ec80-110">พนักงานร้านค้าปลีกสามารถใช้ข้อมูลนี้เพื่อช่วยในการเติมสินค้าตามใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="4ec80-110">The retail store attendant can use this information to facilitate order fulfillment.</span></span>

## <a name="enable-customer-check-in"></a><span data-ttu-id="4ec80-111">เปิดใช้งานการเช็คอินของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="4ec80-111">Enable customer check-in</span></span>

<span data-ttu-id="4ec80-112">เมื่อเปิดคุณลักษณะการเช็คอินของลูกค้า Commerce จะสร้างรหัสการยืนยันใบสั่ง (หรือที่เรียกอีกอย่างว่า รหัสการอ้างอิงช่องทาง)</span><span class="sxs-lookup"><span data-stu-id="4ec80-112">When the customer check-in feature is turned on, Commerce generates an order confirmation ID (also known as the channel reference ID).</span></span> <span data-ttu-id="4ec80-113">นอกจากนี้ ยังสร้างรหัสการยืนยันใบสั่งสำหรับใบสั่งที่ถูกสร้างขึ้นผ่านการขายหน้าร้าน (POS) หรือช่องทางศูนย์บริการด้วย</span><span class="sxs-lookup"><span data-stu-id="4ec80-113">It also generates order confirmation IDs for orders that are created through point of sale (POS) or call center channels.</span></span> 

<span data-ttu-id="4ec80-114">หากต้องการเปิดคุณลักษณะการเช็คอินของลูกค้าในศูนย์ควบคุม Commerce ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="4ec80-114">To turn on the customer check-in feature in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="4ec80-115">ไปที่ **พื้นที่ทำงาน \> การจัดการคุณลักษณะ**</span><span class="sxs-lookup"><span data-stu-id="4ec80-115">Go to **Workspaces \> Feature management**.</span></span>
2. <span data-ttu-id="4ec80-116">ค้นหาคุณลักษณะ **สร้างรูปแบบรหัสการอ้างอิงช่องทางที่สอดคล้องกันระหว่างช่องทางต่างๆ**</span><span class="sxs-lookup"><span data-stu-id="4ec80-116">Search for the **Generate a consistent channel reference ID format across channels** feature.</span></span> 
3. <span data-ttu-id="4ec80-117">เลือกคุณลักษณะ และจากนั้น เลือก **เปิดใช้งานตอนนี้** ในบานหน้าต่างคุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="4ec80-117">Select the feature, and then select **Enable now** in the properties pane.</span></span> 

## <a name="create-a-check-in-confirmation-page"></a><span data-ttu-id="4ec80-118">สร้างหน้าการยืนยันการเช็คอิน</span><span class="sxs-lookup"><span data-stu-id="4ec80-118">Create a check-in confirmation page</span></span>

<span data-ttu-id="4ec80-119">บนไซต์ e-commerce ของคุณ คุณต้องสร้างหน้าใหม่ที่จะหน้าที่เป็นประสบการณ์การยืนยันการเช็คอิน</span><span class="sxs-lookup"><span data-stu-id="4ec80-119">On your e-commerce site, you must create a new page that will serve as the check-in confirmation experience.</span></span> <span data-ttu-id="4ec80-120">โดยผ่านการตั้งค่าคอนฟิกเพิ่มเติม หน้านี้ยังสามารถรวมฟอร์มที่รวบรวมข้อมูลเพิ่มเติมจากลูกค้าเพื่อช่วยในการเติมสินค้าตามใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="4ec80-120">Through additional configuration, the page can also include a form that collects additional information from customers to facilitate order fulfillment.</span></span> <span data-ttu-id="4ec80-121">สำหรับข้อมูลเกี่ยวกับวิธีการตั้งค่าหน้าและโมดูล ดูที่ [โมดูลการเช็คอินของลูกค้า](check-in-pickup-module.md)</span><span class="sxs-lookup"><span data-stu-id="4ec80-121">For information about how to set up the page and module, see [Customer check-in module](check-in-pickup-module.md).</span></span>

## <a name="configure-the-transactional-email-template"></a><span data-ttu-id="4ec80-122">ตั้งค่าคอนฟิกเท็มเพลตอีเมลตามธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="4ec80-122">Configure the transactional email template</span></span>

<span data-ttu-id="4ec80-123">คุณต้องเพิ่มลิงค์ **ฉันอยู่ที่นี่** หรือปุ่มไปยังเท็มเพลตสำหรับอีเมลตามธุรกรรมที่ลูกค้าได้รับ เมื่อใบสั่งที่พร้อมสำหรับจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="4ec80-123">You must add an **I am here** link or button to the template for the transactional email that customers receive when their order is ready for pickup.</span></span> <span data-ttu-id="4ec80-124">ลูกค้าจะใช้ลิงค์หรือปุ่มเพื่อแจ้งให้ร้านค้าทราบว่าพวกเขาได้มาถึงแล้วเพื่อเบิกสินค้าตามใบสั่งซื้อของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="4ec80-124">Customers will use this link or button to notify the store that they have arrived to pick up their order.</span></span> 

<span data-ttu-id="4ec80-125">เพิ่มลิงค์หรือปุ่มลงในเท็มเพลตที่แม็ปกับชนิดการแจ้งเตือน **การบรรจุเสร็จสมบูรณ์** และโหมดการจัดส่งที่คุณใช้สำหรับการเติมสินค้าตามใบสั่งหน้าร้าน</span><span class="sxs-lookup"><span data-stu-id="4ec80-125">Add the link or button to the template that is mapped to the **Packing completed** notification type and the mode of delivery that you're using for curbside order fulfillment.</span></span> <span data-ttu-id="4ec80-126">ในเท็มเพลต ให้สร้างลิงค์หรือปุ่ม HTML ที่ชี้ไปยัง URL ของหน้าการยืนยันการเช็คอินที่คุณสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="4ec80-126">In the template, create an HTML link or button that points to the URL of the check-in confirmation page that you created.</span></span> <span data-ttu-id="4ec80-127">นี่คือตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="4ec80-127">Here is an example.</span></span>

```
<a href="https://[YOUR_SITE_DOMAIN]/[CHECK-IN_CONFIRMATION_PAGE]?channelReferenceId=%channelreferenceid%&channelId=%channelid%&packingSlipId=%packingslipid%" target="_blank">I am here!</a>
```
<span data-ttu-id="4ec80-128">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการตั้งค่าคอนฟิกเท็มเพลตอีเมล โปรดดูที่ [เลือกกําหนดอีเมลธุรกรรมตามโหมดการจัดส่ง](customize-email-delivery-mode.md)</span><span class="sxs-lookup"><span data-stu-id="4ec80-128">For more information about how to configure email templates, see [Customize transactional emails by mode of delivery](customize-email-delivery-mode.md).</span></span> 

## <a name="a-check-in-confirmation-task-is-created-in-pos"></a><span data-ttu-id="4ec80-129">งานการยืนยันการเช็คอินถูกสร้างขึ้นใน POS</span><span class="sxs-lookup"><span data-stu-id="4ec80-129">A check-in confirmation task is created in POS</span></span>

<span data-ttu-id="4ec80-130">หลังจากที่ลูกค้าแจ้งร้านค้าว่าพวกเขามาเพื่อเบิกสินค้าแล้ว ลูกค้าจะได้รับการแจ้งเตือนการยืนยันการเช็คอิน และงานจะถูกสร้างขึ้นในรายการงานใน POS สำหรับร้านค้าที่ลูกค้าเบิกสินค้าตามใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="4ec80-130">After a customer notifies the store that they are present for pickup, they receive a check-in confirmation notification, and a task is created in the tasks list in POS for the store where the customer is picking up the order.</span></span> <span data-ttu-id="4ec80-131">งานมีข้อมูลลูกค้าและใบสั่งทั้งหมดที่ต้องใช้ในการเติมสินค้าให้กับใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="4ec80-131">The task contains all the customer and order information that is required to fulfill the order.</span></span> <span data-ttu-id="4ec80-132">ในงาน ฟิลด์คําแนะนําจะแสดงข้อมูลใดๆ ที่รวบรวมจากลูกค้าผ่านทางฟอร์มข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="4ec80-132">In the task, the instructions field shows any information that was collected from the customer through the additional information form.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="4ec80-133">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="4ec80-133">Additional resources</span></span>

[<span data-ttu-id="4ec80-134">เช็คอินโมดูลการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="4ec80-134">Check-in for pickup module</span></span>](check-in-pickup-module.md)
