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

Initial commitの作成済みタグからReleasesを作成しても、ワークフロー未動作  
<https://github.com/hiren9630/gha-test/releases/tag/release_2023-09-11_3069e51>

ワークフローを作成していたコミットにタグを作成するとpush tagも動作  
最初に作成したリリース時点のタグでは、ワークフローが未作成だったため、動作していなかった  
<https://github.com/hiren9630/gha-test/actions/runs/6156443783>

draft Releasesを作成したが、ワークフロー未動作（リリースノートは自動生成）  
<https://github.com/hiren9630/gha-test/releases/tag/untagged-534a804bf43093e51732>
