# 動作

create-workflowsブランチを作成し、ブランチをpushしただけでcreate tagが動作（未マージ）  
<https://github.com/hiren9630/gha-test/actions/runs/6154263083>

プルリクの作成及びmainへマージ（push）を行ったが、全ワークフロー未動作  
<https://github.com/hiren9630/gha-test/pull/1>  
<https://github.com/hiren9630/gha-test/pull/2>

create tagのワークフローが存在する状態で、新しいブランチを作成してpushすると毎回動作する模様  
<https://github.com/hiren9630/gha-test/actions/runs/6154521556>

作成（remote push）済みのブランチに新しくcommit pushしても特に動作しない

セマンティックバージョニングに基づいたタグを作成しても、全ワークフロー未動作  
<https://github.com/hiren9630/gha-test/releases/tag/v1.0.0>

正規表現にマッチする想定のリリース用タグを作成しても、全ワークフロー未動作  
<https://github.com/hiren9630/gha-test/releases/tag/release_2023-09-11_3069e51>

Initial commitの作成済みタグからReleaseを作成しても、ワークフロー未動作  
<https://github.com/hiren9630/gha-test/releases/tag/release_2023-09-11_3069e51>

ワークフローを作成していたコミットにタグを作成するとpush tagも動作  
最初に作成したリリース時点のタグでは、ワークフローが未作成だったため、動作していなかった  
後から作成したワークフローを、昔のコミットのタグで動かすことは出来なさそう
<https://github.com/hiren9630/gha-test/actions/runs/6156443779>  
<https://github.com/hiren9630/gha-test/actions/runs/6156443783>

draft Releaseを作成したが、ワークフロー未動作（リリースノートは自動生成）  
<https://github.com/hiren9630/gha-test/releases/tag/untagged-534a804bf43093e51732>

タグを作成し、Pre-Releaseを作成（リリースノートは自動生成）  
<https://github.com/hiren9630/gha-test/actions/runs/6156710615>
created releaseとpublished releaseが動作  
<https://github.com/hiren9630/gha-test/actions/runs/6156808572>  
<https://github.com/hiren9630/gha-test/actions/runs/6156808587>

リリース用タグを作成し、Releaseを作成（リリースノートは自動生成）  
<https://github.com/hiren9630/gha-test/actions/runs/6157199502>  
<https://github.com/hiren9630/gha-test/actions/runs/6157199512>  
<https://github.com/hiren9630/gha-test/releases/tag/release_2023-09-12_8b2a55b>  
created releaseとpublished releaseとreleased releaseが動作  
<https://github.com/hiren9630/gha-test/actions/runs/6157224094>  
<https://github.com/hiren9630/gha-test/actions/runs/6157224097>  
<https://github.com/hiren9630/gha-test/actions/runs/6157224728>

## Extra

Release名によって、releasesの順番がどう並ぶのか確認

Releaseを作成  
<https://github.com/hiren9630/gha-test/actions/runs/6157352585>  
<https://github.com/hiren9630/gha-test/actions/runs/6157352592>  
<https://github.com/hiren9630/gha-test/releases/tag/release_2023-09-12_06d607b>  
<https://github.com/hiren9630/gha-test/actions/runs/6157363601>  
<https://github.com/hiren9630/gha-test/actions/runs/6157363612>  
<https://github.com/hiren9630/gha-test/actions/runs/6157363615>

Initial commitの作成済み（Releaseを作成していない方の）タグからLatestではない版のReleaseを作成  
<https://github.com/hiren9630/gha-test/releases/tag/v1.0.0>

draft Releaseをもう一つ作成  
<https://github.com/hiren9630/gha-test/actions/runs/6157513756>  
<https://github.com/hiren9630/gha-test/actions/runs/6157513764>  
<https://github.com/hiren9630/gha-test/releases/tag/untagged-67650277b19a55c2f729>

draft Releaseをもう一つ作成（タグは未作成）  
<https://github.com/hiren9630/gha-test/releases/tag/untagged-33ede38bac603a1c4379>
