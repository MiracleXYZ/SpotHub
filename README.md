# SpotHub

Collaborate on Spotify playlists using GitHub :headphones: :relaxed:

## How does this work?

Using [**GitHub Actions**](https://github.com/features/actions).

On every `push` to the `master` branch, [the Action](https://github.com/swinton/SpotHub/blob/bc2d697744a710bce3ce6a56a10d473045c3ea53/.github/actions/spotify-playlist/Dockerfile) will:

1. [Grab a fresh _access token_ from Spotify](https://github.com/swinton/SpotHub/blob/bc2d697744a710bce3ce6a56a10d473045c3ea53/.github/actions/spotify-playlist/get_access_token.sh)
1. [Generate a JSON payload from `playlist.csv`](https://github.com/swinton/SpotHub/blob/bc2d697744a710bce3ce6a56a10d473045c3ea53/.github/actions/spotify-playlist/process_playlist.sh)
1. [Update a playlist on Spotify](https://github.com/swinton/SpotHub/blob/bc2d697744a710bce3ce6a56a10d473045c3ea53/.github/actions/spotify-playlist/populate_playlist.sh), specified by the `playlist_id` [environment variable](https://developer.github.com/actions/creating-github-actions/accessing-the-runtime-environment/#environment-variables).

## What do I do?

1. Update `playlist.csv`
1. `git commit`
1. `git push`
1. Enjoy your [updated Spotify playlist](https://open.spotify.com/user/stevewinton/playlist/5lNXObovv3WL1Ioyag2FuG) 

## Why was this built?

Because I :heart: Spotify and GitHub, and now I can bring 2 of my favorite things together with [GitHub Actions](https://github.com/features/actions).

Sign up for the GitHub Actions beta [here](https://github.com/features/actions) :headphones: :relaxed:
