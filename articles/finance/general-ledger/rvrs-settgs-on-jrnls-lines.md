---
title: กลับรายการการตั้งค่าในสมุดรายวันและรายการ
description: หัวข้อนี้จะแก้ไขสาเหตุที่รายการที่กลับรายการบัญชีที่ป้อนไว้ในสมุดรายวันทั่วไปอาจไม่รวมอยู่ในธุรกรรมที่ลงรายการบัญชี
author: kweekley
ms.date: 04/29/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-5-05
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 74020f6fc9b0fa8e05a1e2a09fd13dcd60490dc0
ms.sourcegitcommit: 817716c2e96f24af0ef1d7d5323afdeccdc602f3
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/13/2021
ms.locfileid: "6028588"
---
# <a name="reverse-settings-on-journals-and-lines"></a><span data-ttu-id="d8f56-103">กลับรายการการตั้งค่าในสมุดรายวันและรายการ</span><span class="sxs-lookup"><span data-stu-id="d8f56-103">Reverse settings on journals and lines</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d8f56-104">หัวข้อนี้จะแก้ไขสาเหตุที่รายการที่กลับรายการบัญชีที่ป้อนไว้ในสมุดรายวันทั่วไปอาจไม่รวมอยู่ในธุรกรรมที่ลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="d8f56-104">This topic addresses why a reversing entry that was entered on a general journal might not be included on the posted transaction.</span></span>  

## <a name="symptom"></a><span data-ttu-id="d8f56-105">อาการ</span><span class="sxs-lookup"><span data-stu-id="d8f56-105">Symptom</span></span>

<span data-ttu-id="d8f56-106">สมุดรายวันทั่วไปจะรวมรายการที่กลับรายการและวันที่กลับรายการในสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="d8f56-106">A general journal includes a reversing entry and reversing date on the journal.</span></span> <span data-ttu-id="d8f56-107">เมื่อคุณลงรายการบัญชีสมุดรายวัน จะไม่มีการกลับรายการใบสำคัญใด</span><span class="sxs-lookup"><span data-stu-id="d8f56-107">When you post the journal, none of the vouchers are reversed.</span></span> <span data-ttu-id="d8f56-108">สิ่งนี้เกิดขึ้นเพราะเหตุใด</span><span class="sxs-lookup"><span data-stu-id="d8f56-108">Why does this happen?</span></span>

## <a name="resolution"></a><span data-ttu-id="d8f56-109">การแก้ปัญหา</span><span class="sxs-lookup"><span data-stu-id="d8f56-109">Resolution</span></span>

<span data-ttu-id="d8f56-110">เมื่อมีการลงรายการบัญชีสมุดรายวัน กระบวนการกลับรายการจะดูเฉพาะการตั้งค่า **รายการที่กลับรายการ** และ **วันที่กลับรายการ** ในส่วน **รายการ** ของใบสำคัญเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="d8f56-110">When the journal is posted, the reversing process looks only at the **Revering entry** and **Reversing date** settings on the **Lines** section of the voucher.</span></span> <span data-ttu-id="d8f56-111">วิธีการนี้ช่วยให้สมุดรายวันสามารถรวมใบสำคัญบางรายการที่ทำเครื่องหมายไว้สำหรับการกลับรายการและใบสำคัญอื่นๆ ที่ไม่ได้ทำเครื่องหมายได้</span><span class="sxs-lookup"><span data-stu-id="d8f56-111">This approach allows a journal to include some vouchers that are marked for reversing, and others that are not.</span></span>

<span data-ttu-id="d8f56-112">ค่าจากสมุดรายวันจะใช้เป็นค่าเริ่มต้นเมื่อเพิ่มรายการ *ใหม่* เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="d8f56-112">The values from the journal are only used as defaults when adding *new* lines.</span></span> <span data-ttu-id="d8f56-113">การเปลี่ยนค่าในสมุดรายวันไม่ส่งผลกระทบต่อรายการที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="d8f56-113">Changing the values on the journal doesn’t affect existing lines.</span></span> <span data-ttu-id="d8f56-114">ในตัวอย่างนี้ มีการป้อนรายการใบสำคัญก่อน</span><span class="sxs-lookup"><span data-stu-id="d8f56-114">In this example, the voucher lines were entered first.</span></span> <span data-ttu-id="d8f56-115">เมื่อคุณป้อนรายละเอียดรายการก่อนที่จะกำหนดสมุดรายวันเป็นการกลับรายการ การกำหนดเป็นรายการและวันที่ที่กลับรายการจะไม่ใช้กับรายการใดๆ ที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="d8f56-115">When you enter the line detail before designating the journal as reversing, the designation as a reversing entry and date won't be applied to any existing lines.</span></span>

<span data-ttu-id="d8f56-116">การเปลี่ยนรายการที่กลับรายการหรือวันที่กลับรายการในรายการที่มีอยู่จะถ่ายทอดการเปลี่ยนแปลงดังกล่าวไปยังรายการอื่นๆ ในใบสำคัญเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="d8f56-116">Changing the reversing entry or reversing date on an existing line propagates that change to other lines in the same voucher.</span></span> <span data-ttu-id="d8f56-117">เพื่อปรับปรุงประสิทธิภาพการทำงาน ตารางจะไม่รีเฟรชหลังจากถ่ายทอดการเปลี่ยนแปลงไปยังรายการอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="d8f56-117">To optimize performance, the grid is not refreshed after propagating changes to other Lines.</span></span> <span data-ttu-id="d8f56-118">คุณสามารถแสดงค่าที่อัพเดตโดยการรีเฟรชตาราง</span><span class="sxs-lookup"><span data-stu-id="d8f56-118">You can display the updated values by refreshing the grid.</span></span>


