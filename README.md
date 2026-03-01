# n8n UGC Clothing Automation

An automated AI pipeline designed to virtually "dress" models in specific clothing products for high-quality marketing and advertisement creation.

## 🚀 Overview
The **UGC Clothing** workflow allows users to upload a photo of a model and separate photos of clothing items (tops, trousers, shoes). It then uses advanced AI image-to-image editing to realistically overlay those products onto the model while maintaining natural folds, shadows, and branding.

## ✨ Features
- **Flexible Product Input**: Supports varying combinations of products (e.g., just a top, or a full outfit) with dynamic AI prompt logic.
- **High-Fidelity Virtual Try-On**: Utilizes **Fal.ai (Nano-Banana)** to render products with perfect realism and consistent branding.
- **Automated Image Hosting**: Integrates with **imgbb** to instantly convert uploaded files into public URLs for API processing.
- **Smart Resizing**: Features an **Ideogram v3** integration to reframe the final image into specific dimensions like 1024x1024, 1080x1440, or 1920x1080.
- **Async Delivery**: Includes a robust status-checking loop to wait for AI generation to complete before emailing the final result via **Gmail**.

## 🛠️ Requirements
- **n8n** (v1.0+)
- **Fal.ai API Key** (for image editing and reframing)
- **imgbb API Key** (for image hosting)
- **Gmail Credentials** (for automated delivery)

## 📝 Setup
1. Import `UGC Clothing.json` into n8n.
2. Add your **Fal.ai** API key to the HTTP Request nodes (Header Auth).
3. Add your **imgbb** API key to the "Get URL" nodes.
4. Connect your **Gmail** account to the "Send a message" node.
5. Trigger the workflow via the built-in n8n Form.
