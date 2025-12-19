# VeriAnchor IAM Protocol Core
# Deterministic Logic for Zero-Hallucination

def verify_alignment(token_vector, anchor_vector, tau=0.85):
    """
    Checks if the generated token stays within the semantic 
    boundary of the user's intent anchor.
    """
    similarity = calculate_cosine(token_vector, anchor_vector)
    return similarity >= tau
