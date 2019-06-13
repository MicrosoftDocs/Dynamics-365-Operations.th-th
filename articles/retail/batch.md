<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="batch.md" target-language="th-TH">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-d915bc8" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>batch.e70006.4456fc3d5bc4547fa8211642b11ca6df455fa187.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>4456fc3d5bc4547fa8211642b11ca6df455fa187</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>aec1dcd44274e9b8d0770836598fde5533b7b569</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>06/03/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\batch.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Improved handling of batch-tracked items</source><target logoport:matchpercent="0" state="translated">การปรับปรุงให้มีการจัดการสินค้าที่มีการติดตามแบบชุดงาน</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic describes the improvements that have been made to the handling of batches for batch-tracked items during the Retail statement posting process.</source><target logoport:matchpercent="0" state="translated">หัวข้อนี้อธิบายถึงการปรับปรุงที่ดำเนินการกับการจัดการชุดงานของสินค้าที่มีการติดตามแบบชุดงานระหว่างกระบวนการลงรายการบัญชีใบแจ้งยอดการขายปลีก</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Improved handling of batch-tracked items</source>
        <target logoport:matchpercent="0" state="translated" state-qualifier="leveraged-inherited">การปรับปรุงให้มีการจัดการสินค้าที่มีการติดตามแบบชุดงาน</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>In Microsoft Dynamics 365 for Retail Point of Sale (POS), batch numbers can't be captured for batch-tracked items at the time of sale.</source><target logoport:matchpercent="0" state="translated">ในการขายหน้าร้าน (POS) ของ Microsoft Dynamics 365 for Retail ไม่สามารถบันทึกหมายเลขชุดงานสำหรับสินค้าที่มีการติดตามแบบชุดงานในเวลาที่ขาย</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>However, for specific configurations, when sales are posted in the headquarters through customer orders or statement posting, the Microsoft Dynamics system expects that valid batch numbers for batch-tracked items exist, and that they will be used during the invoicing process.</source><target logoport:matchpercent="0" state="translated">อย่างไรก็ตาม สำหรับการตั้งค่าคอนฟิกเฉพาะ เมื่อมีการลงรายการบัญชียอดขายในศูนย์ควบคุมผ่านทางใบสั่งของลูกค้าหรือการลงรายการบัญชีใบแจ้งยอด ระบบ Microsoft Dynamics คาดว่าจะมีหมายเลขชุดงานที่ถูกต้องของสินค้าที่มีการติดตามแบบชุดงาน และระบบจะใช้หมายเลขดังกล่าวในกระบวนการออกใบแจ้งหนี้</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>If valid batch numbers are available for products, the customer order invoicing process and the sales order invoicing process from statement posting use them.</source><target logoport:matchpercent="0" state="translated">หากมีหมายเลขชุดงานที่ถูกต้องของผลิตภัณฑ์ กระบวนการออกใบแจ้งหนี้ใบสั่งของลูกค้าและกระบวนการออกใบแจ้งหนี้ใบสั่งขายจากการลงรายการบัญชีใบแจ้งยอดจะใช้หมายเลขดังกล่าว</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Otherwise, the customer order invoicing process can't post, and the POS user receives an error message.</source><target logoport:matchpercent="0" state="translated">ไม่เช่นนั้น กระบวนการออกใบแจ้งหนี้ใบสั่งของลูกค้าจะไม่สามารถลงรายการบัญชี และผู้ใช้ POS จะได้รับข้อความแสดงข้อผิดพลาด</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Statement posting then goes into an error state.</source><target logoport:matchpercent="0" state="translated">จากนั้นการลงรายการบัญชีใบแจ้งยอดจะเข้าสู่สถานะข้อผิดพลาด</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>This error state occurs even when negative inventory has been turned on for the products.</source><target logoport:matchpercent="0" state="translated">สถานะข้อผิดพลาดนี้จะเกิดขึ้นแม้เมื่อมีการเปิดสินค้าคงคลังติดลบสำหรับผลิตภัณฑ์</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Improvements that have been made in Microsoft Dynamics for Retail version 10.0.4 and later help guarantee that, when negative inventory is turned on for batch-tracked items, customer order invoicing and sales order invoicing through statement posting aren't blocked for those items if the inventory is 0 (zero) or a batch number isn't available.</source><target logoport:matchpercent="0" state="translated">การปรับปรุงที่ดำเนินการใน Microsoft Dynamics for Retail รุ่น 10.0.4 และที่ใหม่กว่าจะช่วยรับประกันว่า เมื่อเปิดสินค้าคงคลังติดลบสำหรับสินค้าที่มีการติดตามแบบชุดงาน การออกใบแจ้งหนี้ใบสั่งของลูกค้าและการออกใบแจ้งหนี้ใบสั่งขายผ่านการลงรายการบัญชีใบแจ้งยอดจะไม่ถูกบล็อคสำหรับสินค้าเหล่านั้นหากสินค้าคงคลังเป็น 0 (ศูนย์) หรือไม่มีหมายเลขชุดงาน</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>The new functionality uses a default batch ID for the sales lines when batch numbers aren't available.</source><target logoport:matchpercent="0" state="translated">ฟังก์ชันใหม่นี้จะใช้รหัสชุดงานเริ่มต้นกับรายการขายเมื่อไม่มีหมายเลขชุดงาน</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>To define the default batch ID that is used for customer orders, on the <bpt id="p1">**</bpt>Retail parameters<ept id="p1">**</ept> page, on the <bpt id="p2">**</bpt>Customer orders<ept id="p2">**</ept> tab, on the <bpt id="p3">**</bpt>Order<ept id="p3">**</ept> FastTab, set the <bpt id="p4">**</bpt>Default batch id<ept id="p4">**</ept> field.</source><target logoport:matchpercent="0" state="translated">หากต้องการกำหนดรหัสชุดงานเริ่มต้นที่ใช้กับใบสั่งของลูกค้า ในหน้า <bpt id="p1">**</bpt>พารามิเตอร์การขายปลีก<ept id="p1">**</ept> บนแท็บ <bpt id="p2">**</bpt>ใบสั่งของลูกค้า<ept id="p2">**</ept> บนแท็บด่วน <bpt id="p3">**</bpt>ใบสั่ง<ept id="p3">**</ept> ให้ตั้งค่าฟิลด์ <bpt id="p4">**</bpt>รหัสชุดงานเริ่มต้น<ept id="p4">**</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>To define the default batch ID that is used for sales order invoicing through statement posting, on the <bpt id="p1">**</bpt>Retail parameters<ept id="p1">**</ept> page, on the <bpt id="p2">**</bpt>Posting<ept id="p2">**</ept> tab, on the <bpt id="p3">**</bpt>Inventory update<ept id="p3">**</ept> FastTab, set the <bpt id="p4">**</bpt>Default batch id<ept id="p4">**</ept> field.</source><target logoport:matchpercent="0" state="translated">หากต้องการกำหนดรหัสชุดงานเริ่มต้นที่ใช้กับการออกใบแจ้งหนี้ใบสั่งขายผ่านการลงรายการบัญชีใบแจ้งยอด ในหน้า <bpt id="p1">**</bpt>พารามิเตอร์การขายปลีก<ept id="p1">**</ept> บนแท็บ <bpt id="p2">**</bpt>การลงรายการบัญชี<ept id="p2">**</ept> บนแท็บด่วน <bpt id="p3">**</bpt>การอัพเดตสินค้าคงคลัง<ept id="p3">**</ept> ให้ตั้งค่าฟิลด์ <bpt id="p4">**</bpt>รหัสชุดงานเริ่มต้น<ept id="p4">**</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>This functionality is available only when advanced warehousing is turned on for the specific store warehouse and items.</source><target logoport:matchpercent="0" state="translated">ฟังก์ชันนี้สามารถใช้ได้เฉพาะเมื่อมีการเปิดการจัดการคลังสินค้าขั้นสูงสำหรับคลังสินค้าและสินค้าของร้านค้าเฉพาะ</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>In a later release, the functionality will also be supported for scenarios where advanced warehouse management isn't used.</source><target logoport:matchpercent="0" state="translated">ในรุ่นถัดไป ฟังก์ชันนี้จะใช้รองรับสถานการณ์ที่ไม่ได้ใช้การจัดการคลังสินค้าขั้นสูงด้วย</target>
        </trans-unit>
      </group>
    </body>
  </file>
</xliff>