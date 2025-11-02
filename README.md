# 📄 PDF Merger Telegram Bot

A fast and efficient Telegram bot for merging PDFs, removing pages, and managing PDF documents - built with Pyrogram and PyMuPDF. **Now with advanced batch processing and reordering capabilities!**

## ✨ Features

### Core Features
- ⚡ **Lightning Fast** - Uses PyMuPDF (5-10x faster than PyPDF2)
- 🔗 **Merge Multiple PDFs** - Combine unlimited PDF files into one
- ✂️ **Remove Pages** - Delete specific pages from any PDF
- 💾 **Smart File Management** - Automatic cleanup of temporary files
- 🎯 **User-Friendly Interface** - Interactive buttons and clear instructions
- 📊 **Real-time Info** - Shows page count and file size
- 🔒 **Session-Based** - Isolated user sessions for privacy

### 🆕 Advanced Features
- 📦 **Batch Upload** - Send 100+ PDFs at once
- 🔄 **Smart Reordering** - Drag and drop style PDF reordering with ⬆️⬇️ buttons
- 📄 **Pagination Support** - View and manage large batches (8 PDFs per page)
- 🔤 **Auto-Sort** - Sort by filename or page count
- 📋 **Order Preview** - See complete PDF list before merging
- 💯 **Large Scale** - Handle 100+ PDFs without message length errors
- 🎨 **Compact Display** - Optimized UI for large file collections

## 🚀 Quick Start

### Prerequisites

```bash
pip install pyrogram tgcrypto PyMuPDF
```

### Setup

1. Get your Telegram API credentials:
   - **API_ID** and **API_HASH** from [my.telegram.org](https://my.telegram.org)
   - **BOT_TOKEN** from [@BotFather](https://t.me/BotFather)

2. Edit the configuration:

```python
API_ID = "YOUR_API_ID"
API_HASH = "YOUR_API_HASH"
BOT_TOKEN = "YOUR_BOT_TOKEN"
```

3. Run the bot:

```bash
python main.py
```

## 📖 Usage

### Basic Workflow
1. Start the bot with `/start`
2. Send PDF files (single or multiple at once)
3. Choose your operation:
   - **View Order & Reorder** - Arrange PDFs before merging
   - **Add More PDFs** - Continue uploading
   - **Merge All PDFs** - Combine into one document
   - **Remove Pages** - Delete specific pages
   - **Download** - Get your final PDF

### Advanced Workflow (Batch + Reorder)
1. Send 10-60+ PDF files (can send all at once)
2. Click **"View Order & Reorder"**
3. Use the reordering interface:
   - ⬆️⬇️ buttons to move PDFs up/down
   - Navigate with **Prev/Next** for large batches
   - **Sort by Name** - Alphabetical ordering
   - **Sort by Pages** - Order by page count
4. Click **"Done"** to confirm order
5. Click **"Done - Merge All"** to merge
6. Download your perfectly ordered merged PDF!

## 🛠️ Commands

- `/start` - Initialize the bot
- `/cancel` - Cancel current operation
- `/help` - Show help message with detailed instructions

## 📋 Configuration

```python
MAX_FILE_SIZE = 100 * 1024 * 1024  # 100MB per PDF (adjustable)
BATCH_TIMEOUT = 30  # seconds to wait for batch uploads
```

## 🔧 Tech Stack

- **[Pyrogram](https://github.com/pyrogram/pyrogram)** - Modern Telegram Bot API framework
- **[PyMuPDF (fitz)](https://github.com/pymupdf/PyMuPDF)** - High-performance PDF library
- **Python 3.8+**

## 📊 Performance

| Operation | PDFs | Time | Notes |
|-----------|------|------|-------|
| Single PDF Processing | 1 | ~1 second | Page removal/editing |
| Batch Merge | 10 PDFs | ~1-3 seconds | Fast PyMuPDF engine |
| Large Batch Merge | 100+ PDFs | ~10-15 seconds | Optimized for large scale |
| Reordering UI | 100+ PDFs | Instant | Paginated interface |

## 🎯 Key Improvements in Latest Version

### Message Length Optimization
- ✅ Fixed `MESSAGE_TOO_LONG` errors for 100+ PDFs
- ✅ Compact display format (30 char filenames)
- ✅ Smart pagination (8 PDFs per page)
- ✅ Callback answer limited to 200 chars

### User Experience
- ✅ Page counter showing position (e.g., "Page 1/8")
- ✅ Quick navigation between pages
- ✅ Status display shows first 5 + last 5 for large batches
- ✅ Instant feedback for all operations

### Scalability
- ✅ Handles 100+ PDFs without crashes
- ✅ Efficient memory management
- ✅ Automatic temp file cleanup
- ✅ Session-based isolation

## 📝 Example Use Cases

1. **Academic Research** - Merge multiple research papers into one document
2. **Legal Documents** - Combine contracts, forms, and agreements
3. **Book Compilation** - Merge chapters into a complete book
4. **Report Assembly** - Combine sections in specific order
5. **Archive Management** - Organize and merge scanned documents

## 🐛 Troubleshooting

### Common Issues

**Bot not responding:**
- Check if API credentials are correct
- Ensure bot token is valid
- Verify internet connection

**File too large error:**
- Reduce PDF file size (compress)
- Check `MAX_FILE_SIZE` setting
- Split into smaller batches

**Merge taking too long:**
- Normal for 60+ PDFs with many pages
- PyMuPDF is already optimized
- Consider splitting into smaller merges

## 📝 License

MIT License - feel free to use and modify!

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 🔮 Planned Features

- [ ] PDF compression option
- [ ] Page range extraction
- [ ] Rotate pages
- [ ] Add watermarks
- [ ] Password protection
- [ ] Split PDFs
- [ ] OCR support

## ⭐ Support

If you found this helpful, give it a star! ⭐

For issues or questions, please open an issue on GitHub.

---

Made with ❤️ using Pyrogram and PyMuPDF

**Latest Update:** Added support for 100+ PDF batch processing with smart pagination and reordering
