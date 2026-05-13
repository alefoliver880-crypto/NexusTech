export default function NexusTechStore() {
  const products = [
    {
      id: 1,
      name: 'Smartphone Ultra X',
      price: 'R$ 2.499',
      image: 'https://images.unsplash.com/photo-1511707171634-5f897ff02aa9?q=80&w=1200&auto=format&fit=crop'
    },
    {
      id: 2,
      name: 'Notebook Pro Vision',
      price: 'R$ 5.999',
      image: 'https://images.unsplash.com/photo-1496181133206-80ce9b88a853?q=80&w=1200&auto=format&fit=crop'
    },
    {
      id: 3,
      name: 'Fone Gamer RGB',
      price: 'R$ 399',
      image: 'https://images.unsplash.com/photo-1505740420928-5e560c06d30e?q=80&w=1200&auto=format&fit=crop'
    },
    {
      id: 4,
      name: 'Smartwatch Future',
      price: 'R$ 899',
      image: 'https://images.unsplash.com/photo-1523275335684-37898b6baf30?q=80&w=1200&auto=format&fit=crop'
    },
    {
      id: 5,
      name: 'Teclado Mecânico Neon',
      price: 'R$ 499',
      image: 'https://images.unsplash.com/photo-1511467687858-23d96c32e4ae?q=80&w=1200&auto=format&fit=crop'
    },
    {
      id: 6,
      name: 'Mouse Gamer Velocity',
      price: 'R$ 249',
      image: 'https://images.unsplash.com/photo-1527864550417-7fd91fc51a46?q=80&w=1200&auto=format&fit=crop'
    }
  ]

  return (
    <div className="min-h-screen bg-zinc-950 text-white">
      <header className="bg-black border-b border-zinc-800 sticky top-0 z-50">
        <div className="max-w-7xl mx-auto flex items-center justify-between px-6 py-4">
          <div>
            <h1 className="text-3xl font-bold tracking-wide text-cyan-400">NexusTech</h1>
            <p className="text-sm text-zinc-400">Sua loja digital de tecnologia</p>
          </div>

          <nav className="hidden md:flex gap-8 text-sm font-medium text-zinc-300">
            <a href="#" className="hover:text-cyan-400 transition">Início</a>
            <a href="#produtos" className="hover:text-cyan-400 transition">Produtos</a>
            <a href="#ofertas" className="hover:text-cyan-400 transition">Ofertas</a>
            <a href="#contato" className="hover:text-cyan-400 transition">Contato</a>
          </nav>

          <button className="bg-cyan-500 hover:bg-cyan-400 text-black px-5 py-2 rounded-2xl font-semibold shadow-lg transition">
            Carrinho
          </button>
        </div>
      </header>

      <section className="relative overflow-hidden">
        <div className="absolute inset-0 bg-gradient-to-r from-cyan-500/20 to-purple-500/20 blur-3xl"></div>

        <div className="max-w-7xl mx-auto px-6 py-24 relative z-10 grid md:grid-cols-2 gap-12 items-center">
          <div>
            <span className="bg-cyan-500/20 text-cyan-300 px-4 py-2 rounded-full text-sm">
              Tecnologia do Futuro
            </span>

            <h2 className="text-5xl md:text-6xl font-black leading-tight mt-6">
              Os melhores eletrônicos em um só lugar.
            </h2>

            <p className="text-zinc-400 mt-6 text-lg leading-relaxed">
              Smartphones, notebooks, acessórios gamers e muito mais com preços incríveis e entrega rápida.
            </p>

            <div className="flex gap-4 mt-8">
              <button className="bg-cyan-500 hover:bg-cyan-400 text-black px-8 py-4 rounded-2xl font-bold text-lg transition shadow-xl">
                Comprar Agora
              </button>

              <button className="border border-zinc-700 hover:border-cyan-400 px-8 py-4 rounded-2xl font-semibold transition">
                Ver Catálogo
              </button>
            </div>
          </div>

          <div>
            <img
              src="https://images.unsplash.com/photo-1519389950473-47ba0277781c?q=80&w=1400&auto=format&fit=crop"
              alt="Tecnologia"
              className="rounded-3xl shadow-2xl border border-zinc-800"
            />
          </div>
        </div>
      </section>

      <section id="produtos" className="max-w-7xl mx-auto px-6 py-20">
        <div className="flex items-center justify-between mb-12">
          <div>
            <h3 className="text-4xl font-bold">Produtos em Destaque</h3>
            <p className="text-zinc-400 mt-2">Os eletrônicos mais vendidos da loja.</p>
          </div>

          <input
            type="text"
            placeholder="Buscar produtos..."
            className="bg-zinc-900 border border-zinc-700 rounded-2xl px-5 py-3 outline-none focus:border-cyan-400"
          />
        </div>

        <div className="grid sm:grid-cols-2 lg:grid-cols-3 gap-8">
          {products.map((product) => (
            <div
              key={product.id}
              className="bg-zinc-900 border border-zinc-800 rounded-3xl overflow-hidden hover:scale-105 transition duration-300 shadow-xl"
            >
              <img
                src={product.image}
                alt={product.name}
                className="h-64 w-full object-cover"
              />

              <div className="p-6">
                <h4 className="text-2xl font-bold">{product.name}</h4>
                <p className="text-cyan-400 text-xl mt-2 font-semibold">{product.price}</p>

                <button className="w-full mt-6 bg-cyan-500 hover:bg-cyan-400 text-black py-3 rounded-2xl font-bold transition">
                  Adicionar ao Carrinho
                </button>
              </div>
            </div>
          ))}
        </div>
      </section>

      <section id="ofertas" className="bg-zinc-900 border-y border-zinc-800 py-20">
        <div className="max-w-7xl mx-auto px-6 text-center">
          <h3 className="text-5xl font-black">Ofertas Exclusivas</h3>
          <p className="text-zinc-400 mt-4 text-lg">
            Receba promoções e descontos especiais diretamente no seu e-mail.
          </p>

          <div className="flex flex-col md:flex-row gap-4 justify-center mt-10 max-w-2xl mx-auto">
            <input
              type="email"
              placeholder="Digite seu e-mail"
              className="flex-1 bg-black border border-zinc-700 rounded-2xl px-5 py-4 outline-none focus:border-cyan-400"
            />

            <button className="bg-cyan-500 hover:bg-cyan-400 text-black px-8 py-4 rounded-2xl font-bold transition">
              Inscrever-se
            </button>
          </div>
        </div>
      </section>

      <footer id="contato" className="max-w-7xl mx-auto px-6 py-10 flex flex-col md:flex-row items-center justify-between gap-4">
        <div>
          <h4 className="text-2xl font-bold text-cyan-400">NexusTech</h4>
          <p className="text-zinc-500 mt-2">© 2026 - Todos os direitos reservados.</p>
        </div>

        <div className="flex gap-6 text-zinc-400">
          <a href="#" className="hover:text-cyan-400 transition">Instagram</a>
          <a href="#" className="hover:text-cyan-400 transition">Facebook</a>
          <a href="#" className="hover:text-cyan-400 transition">WhatsApp</a>
        </div>
      </footer>
    </div>
  )
}
