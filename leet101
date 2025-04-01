class Solution {
public:
    bool isSame(TreeNode* p,TreeNode* q){
        if(p==NULL && q==NULL) return true;
        if(p==NULL || q==NULL) return false;
        if(p->val!=q->val) return false;
        bool leftAns = isSame(p->left,q->left);
        if(leftAns==false) return false;
        bool rightAns = isSame(p->right,q->right);
        if(rightAns==false) return false;
        return true;

    }
    TreeNode* invertTree(TreeNode* root){
        if(root==NULL) return root;
        TreeNode* temp = root->left;
        root->left = root->right;
        root->right = temp;
        invertTree(root->left);
        invertTree(root->right);
        return root;
    }
    bool isSymmetric(TreeNode* root) {
        if(root==NULL) return false;
        invertTree(root->left);
        bool flag = isSame(root->left,root->right);
        invertTree(root->left);
        return flag;
    }
};
