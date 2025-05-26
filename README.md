# inorder
class Solution {
    public static List<Integer> inorder(TreeNode root,List<Integer> result) {
            if (root==null){
                return result;
            }
            inorder(root.left,result);
            result.add(root.val);
            inorder(root.right,result);
            return result;
        }
    public List<Integer> inorderTraversal(TreeNode root) {
        List<Integer> result=new ArrayList<>();
        return inorder(root,result);
    }
}
