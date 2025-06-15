# Giriş
Bu proje, OpenAI Gymnasium ortamlarında çeşitli takviyeli öğrenme (reinforcement learning) algoritmalarının (Deep Q-Learning, PPO, DDPG) uygulanmasını ve karşılaştırılmasını amaçlamaktadır. Projede hem ayrık (FrozenLake, CartPole) hem de sürekli (Pendulum) eylem uzaylarına sahip ortamlar için modern RL algoritmaları kullanılmıştır.

# Metotlar
Deep Q-Learning (DQL) - FrozenLake
Uygulama: qlearning.ipynb
Ana sınıf: FrozenLakeDQL
Replay memory: ReplayMemory
Sinir ağı: DQN sınıfı
Eğitim ve test fonksiyonları: train, test, optimize, print_dqn

DQL algoritması, deneyim tekrar belleği ve hedef ağ kullanılarak uygulanmıştır. Eğitim sırasında elde edilen ödüller ve epsilon değerinin değişimi görselleştirilmiştir.

Proximal Policy Optimization (PPO) - CartPole
Uygulama: ppo.ipynb


Stable Baselines3 kütüphanesi ile PPO algoritması kullanılmıştır. Paralel ortamlar ile eğitim hızlandırılmış, eğitim sonrası model kaydedilip yüklenmiştir. Modelin performansı görselleştirilmiştir.

Deep Deterministic Policy Gradient (DDPG) - Pendulum
Uygulama: ddpg.ipynb
Sürekli eylem uzayına sahip Pendulum ortamında DDPG algoritması uygulanmıştır. Eylem gürültüsü olarak normal dağılım kullanılmış, eğitim sonrası model kaydedilip yüklenmiştir. Modelin ortamda hareketi ve görselleştirilmesi sağlanmıştır.

# Sonuçlar
DQL algoritması ile FrozenLake ortamında başarı oranı ve epsilon azalışı görselleştirilmiştir.
PPO ve DDPG algoritmalarında eğitim sırasında elde edilen kayıplar ve başarılar notebook çıktılarında gözlemlenebilir.
Her algoritma için eğitimli modeller kaydedilmiş ve tekrar yüklenerek test edilmiştir.

# Tartışma
Bu projede, farklı RL algoritmalarının çeşitli ortamlar üzerindeki performansları karşılaştırılmıştır.

DQL, ayrık durum-aksiyon uzaylarında etkili sonuçlar vermiştir.
PPO, paralel ortam desteğiyle hızlı ve stabil öğrenme sağlamıştır.
DDPG, sürekli eylem uzayında başarılı bir şekilde politika öğrenmiştir.
Kodlar modüler ve açıklamalı şekilde yazılmıştır. Her notebook, ilgili ortam ve algoritma için baştan sona eğitim ve test sürecini içermektedir.
