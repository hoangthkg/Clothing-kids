import React, { useState } from "react"; import { Card, CardContent } from "@/components/ui/card"; import { Button } from "@/components/ui/button"; import { Input } from "@/components/ui/input"; const App = () => { const [items, setItems] = useState([]); const [image, setImage] = useState(""); const [title, setTitle] = useState(""); const [price, setPrice] = useState(""); const handleAddItem = () => { if (image && title && price) { setItems([...items, { image, title, price }]); setImage(""); setTitle(""); setPrice(""); } }; return ( 
Quản lý sản phẩm quần áo trẻ em
setImage(e.target.value)} /> setTitle(e.target.value)} /> setPrice(e.target.value)} /> Thêm sản phẩm 
{items.map((item, index) => (   
{item.title}
Giá: ${item.price}
))} 
); }; export default App; 
