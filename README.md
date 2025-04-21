import React from "react";
import { Button } from "@/components/ui/button";
import { Input } from "@/components/ui/input";
import { Card, CardContent } from "@/components/ui/card";
import { Tabs, TabsList, TabsTrigger, TabsContent } from "@/components/ui/tabs";
import { ShoppingCart, PhoneCall, Leaf, Globe, Calendar } from "lucide-react";

export default function LisheMartWebsite() {
  return (
    <div className="p-4 space-y-8">
      {/* Hero Section */}
      <section className="grid md:grid-cols-2 gap-8 items-center">
        <div>
          <h1 className="text-4xl font-bold text-green-800">Rooted in Sustainable Growth. Driven by Impact.</h1>
          <p className="mt-4 text-lg text-gray-700">
            Lishe Mart is your trusted partner in integrated agribusiness, digital innovation, spice production, farm management, and export market facilitation across EAC and SADC regions.
          </p>
          <div className="mt-6 flex gap-4">
            <Button className="bg-orange-600 text-white">Shop Now</Button>
            <Button variant="outline">Book Consultation</Button>
          </div>
        </div>
        <img src="/hero-agri.jpg" alt="Agribusiness" className="rounded-xl shadow-xl" />
      </section>

      {/* Services Tabs */}
      <section>
        <h2 className="text-2xl font-semibold mb-4">Our Services</h2>
        <Tabs defaultValue="tech">
          <TabsList>
            <TabsTrigger value="tech">Agri-Tech</TabsTrigger>
            <TabsTrigger value="advisory">Advisory</TabsTrigger>
            <TabsTrigger value="products">Products</TabsTrigger>
            <TabsTrigger value="trade">Trade & Investment</TabsTrigger>
          </TabsList>
          <TabsContent value="tech">
            <Card><CardContent className="p-4">Smart farming tools, dashboards, traceability, and digital farm services.</CardContent></Card>
          </TabsContent>
          <TabsContent value="advisory">
            <Card><CardContent className="p-4">Farm planning, certification, soil testing, contract farming, and nursery development.</CardContent></Card>
          </TabsContent>
          <TabsContent value="products">
            <Card><CardContent className="p-4">Seeds, seedlings, rhizomes, spice plants, pulses, and input supplies.</CardContent></Card>
          </TabsContent>
          <TabsContent value="trade">
            <Card><CardContent className="p-4">Professional linkages, investment scouting, export readiness and market intelligence.</CardContent></Card>
          </TabsContent>
        </Tabs>
      </section>

      {/* E-commerce Section */}
      <section>
        <h2 className="text-2xl font-semibold mb-4">Order Online</h2>
        <div className="grid md:grid-cols-3 gap-4">
          {["Clove Seedlings", "Turmeric Rhizomes", "Cardamom Plants"].map((item) => (
            <Card key={item} className="hover:shadow-lg">
              <CardContent className="p-4 space-y-2">
                <h3 className="font-semibold text-lg">{item}</h3>
                <p className="text-gray-600">High-quality, certified planting material.</p>
                <Button variant="default" className="w-full"><ShoppingCart className="mr-2 h-4 w-4" />Order Now</Button>
              </CardContent>
            </Card>
          ))}
        </div>
      </section>

      {/* Booking Section */}
      <section className="bg-green-50 p-6 rounded-xl">
        <h2 className="text-2xl font-semibold mb-4">Book a Consultation</h2>
        <div className="grid md:grid-cols-2 gap-4">
          <Input placeholder="Your Name" />
          <Input placeholder="Email or Phone Number" />
          <Input placeholder="Type of Service Interested In" className="md:col-span-2" />
          <Button className="md:col-span-2 bg-orange-600 text-white"><Calendar className="mr-2 h-4 w-4" />Request Booking</Button>
        </div>
      </section>

      {/* Contact Section */}
      <section className="text-center">
        <h3 className="text-lg font-medium">Offices in Morogoro • Kigamboni • Muheza • Mbeya</h3>
        <p className="text-sm text-gray-500">Email: advisory@lishemarts.co.tz | Phone: +255 718 664 645</p>
      </section>
    </div>
  );
}
