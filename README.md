# Giới thiệu về AutoAI-Starter 🚀

_Một khuôn khổ tự động hóa AI tự lưu trữ, được xây dựng trên Bộ khởi động AI tự lưu trữ của nhóm n8n và được cải tiến với Cloudflare, Giao diện người dùng trò chuyện, Cơ sở dữ liệu và RAG._

AutoAI là một bộ công cụ mạnh mẽ được thiết kế để đơn giản hóa việc triển khai và vận hành các Đại lý AI tự động, tận dụng khả năng của n8n và các công nghệ AI tự lưu trữ. Bộ công cụ này tích hợp các thành phần thiết yếu như AI cục bộ, Open WebUI, Flowise, v.v. để hỗ trợ quy trình làm việc AI toàn diện.

## 🌟 Tính năng
- **Tích hợp Cloudflare**: Bảo mật tên miền & tối ưu hóa hiệu suất
- **Chat GUI**: Các cuộc trò chuyện tương tác được hỗ trợ bởi AI
- **Hỗ trợ Database**: Lưu trữ liên tục cho quy trình công việc
- **RAG (Retrieval-Augmented Generation)**: AI thông minh hơn với khả năng truy xuất kiến ​​thức

## 🧪 Cài đặt
1. Sao chép kho lưu trữ này:
```bash
git clone https://github.com/kientranasia/AutoAI-Starter.git
cd AutoAI-Starter
   ```
---
# Bộ khởi động AI tự lưu trữ (by the n8n team)

**Bộ khởi động AI tự lưu trữ** là mẫu docker compose mở
khởi động nhanh chóng một môi trường phát triển AI cục bộ và Low Code
có đầy đủ tính năng bao gồm Open WebUI cho giao diện trò chuyện với các tác nhân N8N của bạn.

Đây là phiên bản của Cole với một vài cải tiến và bổ sung Open WebUI và Flowise!
Ngoài ra, quy trình làm việc của tác nhân AI RAG cục bộ từ video sẽ tự động có trong
phiên bản n8n của bạn nếu bạn sử dụng thiết lập này thay vì thiết lập cơ bản do n8n cung cấp!

[Bộ khởi động AI cục bộ gốc](https://github.com/n8n-io/self-hosted-ai-starter-kit)

Tải xuống tích hợp N8N + OpenWebUI [trực tiếp trên trang web Open WebUI.](https://openwebui.com/f/coleam/n8n_pipe/) (xem thêm hướng dẫn bên dưới)

![n8n.io - Ảnh chụp màn hình](https://raw.githubusercontent.com/n8n-io/self-hosted-ai-starter-kit/main/assets/n8n-demo.gif)

Được tuyển chọn bởi <https://github.com/n8n-io> và <https://github.com/coleam00>, bộ này kết hợp nền tảng n8n tự lưu trữ
với danh sách tuyển chọn các sản phẩm và thành phần AI tương thích để
nhanh chóng bắt đầu xây dựng quy trình làm việc AI tự lưu trữ.

### Bao gồm những gì

✅ [**n8n Self-hosted**](https://n8n.io/) - Nền tảng mã thấp với hơn 400
tích hợp và các thành phần AI tiên tiến

✅ [**Ollama**](https://ollama.com/) - Nền tảng LLM đa nền tảng để cài đặt
và chạy các LLM cục bộ mới nhất

✅ [**Open WebUI**](https://openwebui.com/) - Giao diện giống ChatGPT để
tương tác riêng tư với các mô hình cục bộ và tác nhân N8N của bạn

✅ [**Flowise**](https://flowiseai.com/) - Trình xây dựng tác nhân AI không cần/ít mã
kết hợp rất tốt với n8n

✅ [**Qdrant**](https://qdrant.tech/) - Kho lưu trữ vector hiệu suất cao, mã nguồn mở với API toàn diện

✅ [**PostgreSQL**](https://www.postgresql.org/) - Con ngựa thồ của Thế giới kỹ thuật dữ liệu, xử lý khối lượng dữ liệu lớn một cách an toàn.

## ⚡️ Khởi động nhanh và sử dụng

Thành phần chính của bộ khởi động AI tự lưu trữ là tệp docker compose
được cấu hình sẵn với mạng và đĩa nên bạn không cần phải
cài đặt nhiều thứ khác. Sau khi hoàn tất các bước cài đặt ở trên, hãy làm theo các bước bên dưới
để bắt đầu.

1. Mở <http://localhost:5678/> trong trình duyệt của bạn để thiết lập n8n. Bạn chỉ
phải thực hiện việc này một lần. Bạn KHÔNG tạo tài khoản với n8n trong phần thiết lập ở đây,
đó chỉ là tài khoản cục bộ cho phiên bản của bạn!
2. Mở quy trình làm việc được bao gồm:
<http://localhost:5678/workflow/vTN9y2dLXqTiDfPT>
3. Tạo thông tin xác thực cho mọi dịch vụ:

URL Ollama: http://ollama:11434

Postgres: sử dụng DB, tên người dùng và mật khẩu từ .env. Máy chủ là postgres

URL Qdrant: http://qdrant:6333 (khóa API có thể là bất kỳ khóa nào vì đây là khóa chạy cục bộ)

Google Drive: Thực hiện theo [hướng dẫn này từ n8n](https://docs.n8n.io/integrations/builtin/credentials/google/).
Không sử dụng localhost cho URI chuyển hướng, chỉ cần sử dụng một tên miền khác mà bạn có, nó vẫn hoạt động!
Ngoài ra, bạn có thể thiết lập [trình kích hoạt tệp cục bộ](https://docs.n8n.io/integrations/builtin/core-nodes/n8n-nodes-base.localfiletrigger/).
4. Chọn **Kiểm tra quy trình làm việc** để bắt đầu chạy quy trình làm việc.
5. Nếu đây là lần đầu tiên bạn chạy quy trình làm việc, bạn có thể cần phải đợi
cho đến khi Ollama hoàn tất việc tải xuống Llama3.1. Bạn có thể kiểm tra nhật ký bảng điều khiển docker
để kiểm tra tiến trình.
6. Đảm bảo chuyển quy trình làm việc thành hoạt động và sao chép URL webhook "Sản xuất"!
7. Mở <http://localhost:3000/> trong trình duyệt của bạn để thiết lập Open WebUI.
Bạn chỉ cần thực hiện thao tác này một lần. Bạn KHÔNG tạo tài khoản với Open WebUI trong
phần thiết lập ở đây, đây chỉ là tài khoản cục bộ cho phiên bản của bạn!
8. Vào Không gian làm việc -> Chức năng -> Thêm chức năng -> Đặt tên + mô tả rồi dán
mã từ `n8n_pipe.py`

Chức năng này cũng được [xuất bản tại đây trên trang web của Open WebUI](https://openwebui.com/f/coleam/n8n_pipe/).

9. Nhấp vào biểu tượng bánh răng và đặt n8n_url thành URL sản xuất cho webhook
mà bạn đã sao chép ở bước trước.
10. Bật chức năng và bây giờ chức năng này sẽ khả dụng trong danh sách thả xuống mô hình của bạn ở góc trên bên trái!

Để mở n8n bất kỳ lúc nào, hãy truy cập <http://localhost:5678/> trong trình duyệt của bạn.
Để mở Open WebUI bất kỳ lúc nào, hãy truy cập <http://localhost:3000/>.

Với phiên bản n8n của bạn, bạn sẽ có quyền truy cập vào hơn 400 tích hợp và một
bộ các nút AI cơ bản và nâng cao như
[AI Agent](https://docs.n8n.io/integrations/builtin/cluster-nodes/root-nodes/n8n-nodes-langchain.agent/),
[Text classifier](https://docs.n8n.io/integrations/builtin/cluster-nodes/root-nodes/n8n-nodes-langchain.text-classifier/),
và [Information Extractor](https://docs.n8n.io/integrations/builtin/cluster-nodes/root-nodes/n8n-nodes-langchain.information-extractor/)
nodes. Để giữ mọi thứ cục bộ, chỉ cần nhớ sử dụng nút Ollama cho
mô hình ngôn ngữ và Qdrant làm kho lưu trữ vector của bạn.

> [!LƯU Ý]
> Bộ công cụ khởi động này được thiết kế để giúp bạn bắt đầu với quy trình làm việc AI tự lưu trữ
>. Mặc dù không được tối ưu hóa hoàn toàn cho môi trường sản xuất, nhưng
> nó kết hợp các thành phần mạnh mẽ hoạt động tốt với nhau cho các dự án chứng minh khái niệm
>. Bạn có thể tùy chỉnh để đáp ứng nhu cầu cụ thể của mình
