# Watcher

This is just a rip-off of [tokio](https://github.com/tokio-rs/tokio)'s `tokio::sync::watch` module but using [parking-lot](https://github.com/Amanieu/parking_lot)'s `RwLock` with `arc_lock` and `send_guard` features so that it is `Send` and thus works across `.await` points without triggering rust nightmares.
